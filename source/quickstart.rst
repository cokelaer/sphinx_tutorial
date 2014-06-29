.. _quickstart:

QuickStart
===========

Installation
-------------

Before starting, you first need to install Sphinx, which is done very easily using **easy_install** or **pip** command in a command shell::

    pip install sphinx --upgrade

.. note:: Most Linux distributions provide sphinx in their repository therefore if easy_install (or pip) does not work, you may try yum (Fedora) or apt-get (ubuntu).


Create your own sphinx project
--------------------------------

Once **sphinx** is installed, you can start a new sphinx project. In a shell, type::

    sphinx-quickstart

and follow the instructions. Most of the time you simply need to press enter. 


However, you will have to enter the project name, your name, the version (put 1 if you don't know) and select the extension that you will need later on (.txt or .rst to your conveninence but I would recommend rst). If you do not know, select *yes* to all (note that jsmath raised an error on my distributution). 

.. note:: this is a basic setup. All options will be stored in a file called **conf.py**, which can be edited at any time later on.

In principle you should now have a file called **conf.py**, a file called **index.rst** (or contents.rst) and some directories.


The **conf.py** file can be edited if you know what you are doing so as to add new extensions, additional html pages, change the authors or version and much more. Here below is the beginning of the conf.py file used to create this documentation:

.. literalinclude:: conf.py
    :linenos:
    :language: python
    :lines: 1-30

The file **index.rst** is your entry point. Change it to your need.

Next time you want to create a project, you can just copy the **conf.py** and makefiles into a new directory.

Compilation
------------

In order to compile the documentation, under linux type::

    make html

or::

    make latex

and under windows, type::

    make.bat html


This command will analyse the files in the source/ directory and create the HTML files into the directory **_build/html/**  or  **build/html** depending on your configuration file.



There are many more possible outputs. Type **make** without argument to get help. For example, to build a PDF version, type::

    make latexpdf


Now, it is time to edit your main file **index.rst** or **contents.rst** and to learn about the RST and Sphinx syntaxes.

