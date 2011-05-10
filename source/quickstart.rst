.. _quickstart:

QuickStart
===========

Installation
-------------

Before starting, you first need to install Sphinx, which is done very easily using easy_install in a command shell::

    easy_install -U sphinx

.. note:: The -U is used to make sure that you update the version you have (if already installed)



Create your own sphinx project
------------------------------
If you want to start your own documentation with Sphinx, the simplest way is to initialise a new project. Type::

    sphinx-quickstart

and follow the instructions. Most of the time you simply need to press enter. 


However, you will have to enter the project name, your name, the version (put 1 if you don't know) and select the extension that you will need later on. If you do not know, select *yes* to all (except jsmath, which raise error on my version). 

.. note:: this is a basic setup. All options will be stored in a file called **conf.py**, which can be edited at any time later on.

In principle you should now have a file called **conf.py**, a file called **index.rst** (or contents.rst) and some directories.


The **conf.py** file can be edited if you know what you are doing so as to add new extensions, additional html pages, ...

.. literalinclude:: conf.py
    :linenos:
    :language: python
    :lines: 1-15

The file **index.rst** is your entry point. Change it to your need.

Compilation
------------

In order to compile the documentation, under linux type::

    make html

or::

    make latex

and under windows, type::

    make.bat html

The built HTML pages are in the directory **_build/html/** by default.

To build a PDF version, type the previous command and then::

    cd _build
    make all-pdf



Now, it is time to edit your main file **index.rst** or **contents.rst** and to learn about the RST and Sphinx syntaxes.

