YAML2RPM Documentation
======================

Welcome to the documentation for YAML2RPM.

The documentation explains how you can create an initial setup 
structure and then provides instructions to build, update 
and create new admixes (loose collections) for building RPMS
for the scientifics software.

It also includes a Reference section which provides quick information on several topics.
**yaml2rpm** is a Python code that users yaml template files describing how
a specific package is to be built. 
It shows our recipes  from the created repositories in `RCIC Public  <https://github.com/RCIC-UCI-Public />`_
and offers a *simple* and *intuitive* API.

Check out the :doc:`usage` section for further information, including
how to :ref:`installation` the project.

**yaml2rpm** has its documentation hosted on Read The Docs.

.. note::

   This project is under active development.

.. toctree::
   :glob:
   :caption: ABOUT YAML2RPM

   about/preface
   about/architecture

.. toctree::
   :caption: INSTALLATION

   requirements
   usage
   api
   gcc
