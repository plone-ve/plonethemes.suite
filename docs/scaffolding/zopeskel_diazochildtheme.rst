.. _zopeskel-diazochildtheme:

zopeskel.diazochildtheme
------------------------

The `zopeskel.diazochildtheme v0.1`_ package include ``Paster`` templates for Plone 
`diazotheme.frameworks`_ bootstrap childtheme package.

diazochildtheme
^^^^^^^^^^^^^^^

This is a :ref:`ZopeSkel <zopeskel>` template package for creating a skeleton Plone add-on
package. The skeleton package creates a :ref:`Bootstrap <bootstrap-css-framework>` Diazo 
(``diazotheme.frameworks``) childtheme package and associated css and js resources for use 
with `plone.app.theming`_ in Plone 4.2+.

Use this package when you want to package a Diazo childtheme as a Plone add on,
particularly if you need to override viewlet or skin templates in the process.

.. note::
    This is a development tool. You should be familiar with Plone and buildout to
    use it.

.. warning::
   This package is compatible with ``ZopeSkel < 3.0`` only.

Usage
`````

Add-ons under development are typically created in your buildout's ``src`` directory. 
Command line for creating a package named ``diazochildtheme.mychildtheme`` would be:

::

  $ cd src/ && ../bin/zopeskel diazochildtheme diazochildtheme.mychildtheme

This will create a Python package with a directory structure like this::

    diazochildtheme.mychildtheme/
    |-- diazochildtheme
    |   +-- mychildtheme
    |       |-- diazo_resources
    |       |   +-- static
    |       |-- locales
    |       |-- profiles
    |       |   +-- default
    |       +-- template_overrides
    |-- diazochildtheme.mychildtheme.egg-info
    +-- docs

The typically customized parts are in the follow subdirectory 
``diazochildtheme.mychildtheme/diazochildtheme/mychildtheme`` .


----

.. _`plone.app.theming`: https://pypi.org/project/plone.app.theming/1.1.8/
.. _`zopeskel.diazochildtheme v0.1`: https://pypi.org/project/zopeskel.diazochildtheme/0.1/
.. _`diazotheme.frameworks`: https://github.com/collective/diazotheme.frameworks
