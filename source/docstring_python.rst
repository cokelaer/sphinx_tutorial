.. _docstring_python:


Example on how to document your Python docstrings
######################################################


.. topic:: Overview

    This example shows how to document your docstrings and how to interpret it within your RST document.

    :Date: |today|
    :Author: **Thomas Cokelaer**


.. module:: template

Let us consider a python module called :mod:`template` (see bottom of the page).
With Sphinx, you can auto-document this module by including the following code within a RST document::


    .. automodule:: template
        :members:
        :undoc-members:
        :inherited-members:
        :show-inheritance:

This code will scan the module template.py, find all its members, undocumented members and add their docstrings. It will also include documentation from inhereted classes (if any) and show the inheritance tree. 

.. warning :: Your modules must be visible that is partof your PYTHONPATH variable otherwise Sphinx is not able to find them.


There is a lot of tunable possibilities. For instance, you can include only some members if needed.



-----

Auto documented class (method 1)
--------------------------------

The previous code generates automatically the following documentation for the class MainClass1 contained in the module template.py

.. automodule:: template
   :members: 
   :undoc-members:
   :inherited-members:
   :show-inheritance:




template.py source file
-----------------------
The source file is provided for convience here below:


.. literalinclude:: template.py
   :linenos:
   :language: python


