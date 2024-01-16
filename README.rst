Package Information
==============================

Some information here.

Table of contents
-----------------

.. contents:: 


Header number one
------------------------
Bla Bla Bla.  

Bla Bla Bla.

.. code-block:: raw
   
   project_name
   ├── docs
   │   ├── make.bat
   │   ├── Makefile
   │   └── source
   │       ├── conf.py
   │       └── index.rst
   ├── examples
   │   └── example.py
   ├── src
   │   └── package_name
   │       └── __init__.py
   ├── tests
   │   └── __init__.py
   ├── .gitignore
   ├── LICENSE.txt
   ├── MANIFEST.in
   ├── README.rst
   ├── requirements.txt
   ├── setup.cfg
   ├── setup.py
   └── tox.ini

Bla Bla Bla.

Header number ``two``
^^^^^^^^^^^^^^^^^^^

The ``setup.py``, ``setup.cfg`` and ``MANIFEST.in`` files are used to
specify how a package should be installed. You might think that you don't
want to create an installable package, so let's skip this. DON'T! Even for
small projects, you should include these because of something called
editable installs (more on that later). The most basic setup.py file should
look like this

.. code-block:: python

   from setuptools import setup

   setup()
