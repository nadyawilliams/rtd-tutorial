Template for the Read the Docs tutorial
=======================================

This GitHub template includes fictional Python library
with some basic Sphinx docs:

- read the tutorial : https://docs.readthedocs.io/en/stable/tutorial/
- tutorial template github  https://github.com/readthedocs/tutorial-template/

This test documentation:

- github repo https://github.com/nadyawilliams/rtd-tutorial
- website docs https://npw-rtd-tutorial.readthedocs.io/en/latest/index.html
- readthedocs dashboard https://readthedocs.org/dashboard/npw-rtd-tutorial

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


optional yamldoc sphinx integration
-----------------------------------

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

Using yamldoc locally to create md files is ok, however 
Main build on read the docs fails in importing sphinx_markdown_tables
module. Comment out in conf.py
