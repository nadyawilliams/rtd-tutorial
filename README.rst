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

Point your browser to `build/html/index.html`.

