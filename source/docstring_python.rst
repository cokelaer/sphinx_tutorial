.. _docstring_python:


How to document your Python docstrings
#######################################


.. topic:: Overview

    This example shows how to document your docstrings and how to interpret it within your reST document.

    :Date: |today|
    :Author: **Thomas Cokelaer**


.. module:: template

Let us consider a python module :mod:`template` module.
With Sphinx, you can auto-document this module by typing::


    .. automodule:: template.py
        :members:
        :undoc-members:
        :inherited-members:
        :show-inheritance:

.. warning :: make sure your modules are inside your PYTHONPATH otherwise Sphinx is not able to parse them.


The :mod:`template` module contains a class :class:`MainClass1` and its method :meth:`function1 <MainClass1.function1>`.

Alternatively, if you do not want to auto document the entire module but only a class, you would proceed as follows::

    .. autoclass:: template.MainClass1
       :members: 
       :undoc-members:
       :inherited-members:
       :show-inheritance:


-----

Auto documented class (method 1)
--------------------------------

.. autoclass:: MainClass1
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


