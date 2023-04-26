Template for the Read the Docs tutorial
=======================================

This GitHub template includes fictional Python library
with some basic Sphinx docs.

Read the tutorial here:

https://docs.readthedocs.io/en/stable/tutorial/


Building HTML locally for testing
---------------------------------

1. Install prerequisites

   .. code-block:: console

      pip install sphinx
      pip install sphinx_rtd_theme


2. Check out repo and build

   .. code-block:: console

      git clone https://github.com/nadyawilliams/rtd-tutorial
      cd rtd-tutorial/docs
      make html

3. Point your browser to `build/html/index.html`.


4. optional yamldoc sphinx integration

   This is for reference only. The integration is described in
   http://chrisbcole.me/yamldoc/sphinx/

   However it does not support autosummary-like inclusion of python or other
   language files.

   Keep for a reference

   .. code-block:: console

      pip3 install recommonmark
      pip3 install sphinx-markdown-tables
      pip3 install yamldoc

   Edit conf.py file per above link info

   Create md files from yaml files via

   .. code-block:: console

      yamldoc file.yaml > file.md
