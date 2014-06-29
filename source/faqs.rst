FAQS
==========


The link do not appear correctly when using :class: directive
-------------------------------------------------------------

The class you try to reference is not included in any of your rst files. 

For instance, if you try to access the class *square*  in the module *math*, which is a standard python module, you still need somewhere to have that module included with e.g. the automodule command::

    .. automodule:: math

.. _How_to_create_an_internal_reference:

How to create an internal reference
-----------------------------------

First, you need to create a label in the text wherever you want the reference to jump to. Here, we place such a label just before the title (see source file) using this syntax::

    .. _How_to_create_an_internal_reference:


Then, use the :ref: keyword and reference name as follows::

    :ref:`How_to_create_an_internal_reference`


So, in the text, it will simply appears like that: :ref:`How_to_create_an_internal_reference`.


This is not satisfactory because the name is not great. So, you can replace it as follows::


    :ref:`nicer reference <How_to_create_an_internal_reference>`

    
which renders as follows :ref:`nicer reference <How_to_create_an_internal_reference>`


Get section numbers
-------------------

Give a :numbered: option to the toctree directive where you want to start numbering.::

    .. toctree::
       :numbered: 1
