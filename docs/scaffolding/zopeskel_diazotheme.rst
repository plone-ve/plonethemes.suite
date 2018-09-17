.. _zopeskel-diazotheme:

zopeskel.diazotheme
-------------------

The `zopeskel.diazotheme v1.1`_ package contains the following :ref:`ZopeSkel <zopeskel>` templates:


diazotheme
^^^^^^^^^^

This is a :ref:`ZopeSkel <zopeskel>` template package for creating a skeleton Plone add-on package. 
The skeleton package creates a Diazo (`plone.app.theming`_) theme package and 
associated css and js resources for use with ``plone.app.theming`` package in Plone 4.2+.

Use this package when you want to package a Diazo theme as a Plone add on,
particularly if you need to override viewlet or skin templates in the process.

.. note::
    This is a development tool. You should be familiar with Plone and buildout to
    use it.

Usage
`````

For use the ``diazotheme`` :ref:`ZopeSkel <zopeskel>` template, execute the follow command 
and response the questions in the standard input from the console command:

::

    $ cd src/ && ../bin/zopeskel diazotheme diazotheme.mytheme

This will create a Python package with a directory structure like this::

    diazotheme.mytheme/
    |-- diazotheme
    |   +-- mytheme
    |       |-- diazo_resources
    |       |   +-- static
    |       |-- locales
    |       |-- profiles
    |       |   +-- default
    |       +-- template_overrides
    |-- diazotheme.mytheme.egg-info
    +-- docs

The typically customized parts are in the follow subdirectory 
``diazotheme.mytheme/diazotheme/mytheme`` .

----

.. _`plone.app.theming`: https://pypi.org/project/plone.app.theming/1.1.8/
.. _`zopeskel.diazotheme v1.1`: https://pypi.org/project/zopeskel.diazotheme/1.1/
