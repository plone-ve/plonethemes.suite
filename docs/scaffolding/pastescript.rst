.. _pastescript:

PasteScript
-----------

The `PasteScript v1.7.5`_ package is a pluggable command-line frontend, including 
commands to setup package file layouts. This package generate a script called 
``paster``. This script allows you to create the file layout for a Python distribution.

Creating a new project. Projects are typically Python packages, ready for
distribution. Projects are created from templates, and represent different
kinds of projects -- associated with a particular framework for instance.

.. note::
    This is a development tool. You should be familiar with Plone and buildout to
    use it.


create a new project with paster script
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can create a new project using the ``paster`` script, executing the follow command:

::

    $ cd src/ && ../bin/paster create -t TEMPLATE YOUR.PROJECT


list templates from paster script
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can list the :ref:`ZopeSkel <zopeskel>` templates available using the ``paster`` 
script, executing the follow command:

::

    $ cd src/ && ../bin/paster create --list-templates


paster script help 
^^^^^^^^^^^^^^^^^^

You can read the ``paster`` help available, executing the follow command:

::

    $ ./bin/paster --help

----

.. _`PasteScript v1.7.5`: https://pypi.org/project/PasteScript/1.7.5/
