Architecture
=============

.. _architecture:


Python scripts
--------------

There is one main driver scipt called ``gen-definitions.py``
This is the definitions parser that reads info defined in yaml files and creates
necessary output files in order to build RPMS.


Templates
---------

There are a few Makefils that are used as templates when crating packages

In additon, there are a few templates writtien in yaml that provide basic 
configuratio and settings. These templates are included in the 
specific software yaml description files



