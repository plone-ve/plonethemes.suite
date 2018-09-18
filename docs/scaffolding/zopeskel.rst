.. _zopeskel:

ZopeSkel
--------

The `ZopeSkel v2.21.2`_ package include the templates and code generator for 
quickstarting Plone/Zope projects. This package generate a script called 
``zopeskel``. This script allows you to create basic skeletons for plone and 
zope products and buildouts based on best-practice templates.

It is a wrapper around :ref:`PasteScript <pastescript>` (``paster``), providing 
an easier syntax for invoking and better help.

.. note::
    This is a development tool. You should be familiar with Plone and buildout to
    use it.


create a new project with zopeskel script
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can create a new project using the ``zopeskel`` script, executing the follow 
command:

::

    $ ./bin/zopeskel TEMPLATE YOUR.PROJECT


list templates from zopeskel script
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can list the :ref:`ZopeSkel <zopeskel>` templates available using the ``zopeskel`` 
script, executing the follow command:

::

    $ ./bin/zopeskel --list


zopeskel script help 
^^^^^^^^^^^^^^^^^^^^

You can read the ``zopeskel`` help available, executing the follow command:

::

    $ ./bin/zopeskel --help

----

.. _`ZopeSkel v2.21.2`: https://pypi.org/project/ZopeSkel/2.21.2/
