.. _doctest:



How to include test in your Python docstrings using doctest
==============================================================

.. topic:: Overview

    This page describes the special directive **doctest**

    :Date: |today|
    :Author: **Thomas Cokelaer**



quickstart
-----------
you may want to include test directly within your RST documents or Python docstring as follows::

    .. doctest::

        >>> import math
        >>> print math.sqrt(2.)
        1.41421356237

which will be displayed like that:

.. doctest::

    >>> import math
    >>> print math.sqrt(2.)
    1.41421356237

You can check that the code included that way is correct: in the shell, instead of compiling the HTML doc, type::

    make doctest

See ` <http://docs.python.org/library/doctest.html>`_ for a complete description

Analysing the code above, the '>>>' sign means `run the command that follows`. 
If a command returns a value then the next line must contain the expected results otherwise 
an error occurs. This is why we put the results of square root 2 above. 


+SKIP option
-------------
Now, you may say that you do not know the expecting result or do not care about it or it may be random. In such case, you ant to skip the correctness of the output. Add this comment:
**#doctest: +SKIP**
    

    .. doctest::

        >>> import math
        >>> print math.log(20.) #doctest: +SKIP

which will be displayed like that:

.. doctest::

    >>> import math
    >>> math.log(20.) #doctest: +SKIP

What's happen here is that the first line is tested, the second one is ran but the validity of the result is not tested.


If you want to skip all the commands (better to use a code-block directive in such case though), then type::

    .. doctest::
        :options: +SKIP

        >>> whatever code




