Preface
=====

.. _installation:

Yaml2rpm
------------

Generic Methodology for building RPMS
This software uses the underlying Rocks methodology for automatically creating RPM spec
files to create packages.  Where it differs from Rocks is that a
YAML-based specification of a package is used to define the specific details of a
component, instead of a subdirectory structure for each package (see the rocksclusters github rolls for many examples of the subdirectory structure.

Most (open-source) software starts with a source tarball, extracts the tarball, 
configures for the local environment,  executes "make" and then executes "make install".
In the above, "make" might be "cmake" or some other software-specific tool. The last step,
to turn the result of the above, community-standard, process into an installable package
is often deemed too time-consuming or difficult. The advantages of creating a package include:
  - File system conflicts resulting from different software builds are flagged prior-to-install
  - Software dependency resolution staves off many errors when attempting to remove
    a key software package that other packages depend upon
  - Binary packages can be "compiled once" and reused in testing, staging, production 
    environments
  - System tools (e.g., yum) can be used a common tool to interrogate the file system for
    integrity, ownership of specific files and other items.

This software relies on only one Rocks-created software package, but otherwise is completely compatible with Generic CentOS (And RedHat). 

Motivation
------------
The approach used here is one where programmatic translations are used to progressively create a subdirectory structure that mirrors the way Rocks (an example of building a qrencode RPM -  https://github.com/rocksclust
ers/base/blob/master/src/qrencode) builds RPMS.  In that structure, an RPM spec file is automatically created and files are put in appropriate places in which rpmbuild (https://linux.die.net/man/8/rpmbuild) can success
fully build a package.  The generated spec file must define a source in a %source as well as %build, %install, %file and other RPM-specific directives.  In particular, the %source is a tarball of this directory in gith
ub (e.g. the base/src/qrencode directory). However, prior to creating the tarball, the upstream tarball (e.g. qrencode-3.4.0.tar.bz2) must be placed in base/src/qrencode directory.  The automatically generated spec fil
e, the `%build` directive invokes the `build` target of the Makefile provided here.   In this example the section looks like:

.. code-block:: console

   build:
	   bunzip2 -c $(NAME)-$(VERSION).$(TARBALL_POSTFIX) | $(TAR) -xf -
	   ( 							\
		cd $(NAME)-$(VERSION);				\
		./configure --prefix=$(PKGROOT); 		\
		$(MAKE);					\
	   )


Example of block command

.. code-block:: console

   (.venv) $ pip install lumache

Quickstart
----------------

If you want to use prebuilt RPMS for testing on a standard CentOS machine, you can follow what is below. The following was
tested on the official CentOS 7 Amazon machine image.

If you want to build yaml2rpm RPMS and install them from source repo, see Building
### Prerequisites

(1) Python 2 or 3. Required python modules: argparse, socket, datetime. There are 4 python modules that will be automatically
   built and installed during the "Building" step:

   - future: for compatibility of python 2/3 code
   - ruamel-yaml & ruamle-ycml-clib: used by the  main script gen-definitions.py
   - setuptools: for build python dependent packages.

(2) If you are using a very stripped-down CentOS image (similar to the official CentOS 7 image in Amazon, you will
    want to make certain you have the following packages and package groups installed
   
    ::

       yum groupinstall "Development Tools" "Console Internet Tools"
       yum install redhat-lsb wget zlib-devel environment-modules
       . /etc/profile.d/modules.sh

