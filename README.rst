Package Information
==============================

Also, this tutorial will always be a work in progress (or at least so long
as best practice can change), so the tutorial might change at any time.
However, you can always read old versions of the tutorial,  since it is
covered by source control. Finally, if you have any constructive critic on the
contents in this tutorial, please raise an Issue with the Issue tracker.

Table of contents
-----------------

.. contents:: 


Structuring a repository
------------------------
An integral part of having reusable code is having a sensible repository
structure. That is, which files do we have and how do we organise them.
Unfortunately, figuring out how to structure a Python project best is not
a trivial task. In this part of the tutorial, I hope to show you a way
to initate any Python project to ensure that you won't have to do major
effort restructuring the code once you want to publish it.  

Let us start with the folder layout. Your project directory should
be structured in the following way and we will explain why later.

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

Now, this is a lot of files, let us look at these to understand what the
different components are and why they are necessary in a Python project.

The ``setup`` files
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