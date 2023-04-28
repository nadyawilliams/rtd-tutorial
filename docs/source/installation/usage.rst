Usage
=====

.. _usage:

Installation
------------

To use Lumache, first install it using pip:

.. code-block:: console

   (.venv) $ pip install lumache

This is an example of using just the double colon::

   ls -l
   pwd


This is an example of code block with language:

.. code-block:: bash

   ls -l
   pwd
   conda config --add channels defaults
   conda config --add channels conda-forge

Creating recipes
----------------

This is coming from lumanch.py file

To retrieve a list of random ingredients,
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']


add python source file as an example

.. literalinclude:: files/new.py
   :language: python

add bash source file as an example

.. literalinclude:: files/xmodl
   :language: bash

.. literalinclude:: files/ex.yaml
   :language: yaml

List
-------------
* This is a bulleted list.
* It has two items, the second
  item uses two lines.

1. This is a numbered list.
2. It has two items too.

#. This is a numbered list.
#. It has two items too.


Nested list
------------
* this is
* a list

  * with a nested list
  * and some subitems

* and here the parent list continues

Table
------

+------------------------+------------+----------+----------+
| Header row, column 1   | Header 2   | Header 3 | Header 4 |
| (header rows optional) |            |          |          |
+========================+============+==========+==========+
| body row 1, column 1   | column 2   | column 3 | column 4 |
+------------------------+------------+----------+----------+
| body row 2             | ...        | ...      |          |
+------------------------+------------+----------+----------+

Links
-----

Use `Link text <https://domain.invalid/>`_ for inline web links. 
If the link text should be the web address, you don’t need special markup at all, the parser finds links and mail addresses in ordinary text.

You can also separate the link and the target definition (ref), like this:

This is a paragraph that contains `a link`_.

.. _a link: https://domain.invalid/


This example is fro mthe top tutorial of read the docs
The tutorial is aimed at people interested in learning
how to use Read the Docs to host their documentation projects.
You will fork a fictional software library
similar to the one developed in the :doc:`official Sphinx tutorial <sphinx:tutorial/index>`.
No prior experience with Sphinx is required
and you can follow this tutorial without having done the Sphinx one.

Trying the popup text

Read the Docs will try to build the documentation of your project
right after you create it.
To see the build logs,
click on the :guilabel:`Your documentation is building` link on the :term:`project home`,
or alternatively navigate to the :guilabel:`Builds` page,


Trying a note:

.. tip::

	We strongly recommend :doc:`pinning all the versions </installation/api>` required to build the documentation to avoid unexpected build errors.

.. attention::

	We strongly recommend reading the :doc:`pinning all the versions </about/architecture>` 

.. note::

	This is a simple note 


Button
-------

trying from tutorial text snippet
here you will see a green :guilabel:`Use this template` button.
Click it to open a new page that will ask you for some details:

TEXT
------

This is the repository you will import on Read the Docs,
and it contains the following files:

``README.rst``
  Basic description of the repository, you will leave it untouched.

``pyproject.toml``
  Python project metadata that makes it installable.
  Useful for automatic documentation generation from sources.

``lumache.py``
  Source code of the fictional Python library.

``docs/``
  Directory holding all the Sphinx documentation sources,
  including the Sphinx configuration ``docs/source/conf.py``
  and the root document ``docs/source/index.rst`` written in reStructuredText.


Figures 
--------

This is made with figure

.. figure:: /installation/images/usageStats.png
   :width: 80%
   :align: center
   :alt: Usage stats 

   Usage stats image 


This is made with image

.. image :: images/loadStats.png
