.. _scaffolding-tools:

Scaffolding tools
=================

.. todo::
    TODO write about Scaffolding tools and his values for create Plone theme packages. 


The **"Plone theming suite"** includes the following scaffolding tools supported:

- :ref:`ZopeSkel <zopeskel>`. 

- :ref:`PasteScript <pastescript>`.

- :ref:`zopeskel.diazochildtheme <zopeskel-diazochildtheme>`.

- :ref:`zopeskel.diazotheme <zopeskel-diazotheme>`.

- :ref:`vs.zopeskel.diazo <vs-zopeskel-diazo>`.

- :ref:`toutpt.zopeskel <toutpt-zopeskel>`.


.. _zopeskel:

ZopeSkel
--------

The `ZopeSkel v2.21.2`_ package include the templates and code generator for 
quickstarting Plone/Zope projects. This package generate a script called 
``zopeskel``. This script allows you to create basic skeletons for plone and 
zope products and buildouts based on best-practice templates.

It is a wrapper around :ref:`PasteScript <pastescript>` (``paster``), providing 
an easier syntax for invoking and better help.


create a new project with zopeskel script
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can create a new project using the ``zopeskel`` script, executing the follow command:

::

    $ ./bin/zopeskel TEMPLATE YOUR.PROJECT


list templates from zopeskel script
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can list the :ref:`ZopeSkel <zopeskel>` templates available using the ``zopeskel`` script, 
executing the follow command:

::

    $ ./bin/zopeskel --list


zopeskel script help 
^^^^^^^^^^^^^^^^^^^^

You can read the ``zopeskel`` help available, executing the follow command:

::

    $ ./bin/zopeskel --help

----

.. _pastescript:

PasteScript
-----------

The `PasteScript v1.7.5`_ package is a pluggable command-line frontend, including 
commands to setup package file layouts. This package generate a script called 
``paster``. This script allows you to create the file layout for a Python distribution.

Creating a new project. Projects are typically Python packages, ready for
distribution. Projects are created from templates, and represent different
kinds of projects -- associated with a particular framework for instance.


create a new project with paster script
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can create a new project using the ``paster`` script, executing the follow command:

::

    $ cd src/ && ../bin/paster create -t TEMPLATE YOUR.PROJECT


list templates from paster script
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can list the :ref:`ZopeSkel <zopeskel>` templates available using the ``paster`` script, executing the 
follow command:

::

    $ cd src/ && ../bin/paster create --list-templates


paster script help 
^^^^^^^^^^^^^^^^^^

You can read the ``paster`` help available, executing the follow command:

::

    $ ./bin/paster --help

----

.. _zopeskel-diazochildtheme:

zopeskel.diazochildtheme
------------------------

The `zopeskel.diazochildtheme v0.1`_ package include ``Paster`` templates for Plone 
`diazotheme.frameworks`_ bootstrap childtheme package.

This is a :ref:`ZopeSkel <zopeskel>` template package for creating a skeleton Plone add-on
package. The skeleton package creates a Bootstrap Diazo (``diazotheme.frameworks``) 
childtheme package and associated css and js resources for use with `plone.app.theming`_  
in Plone 4.2+.

Use this package when you want to package a Diazo childtheme as a Plone add on,
particularly if you need to override viewlet or skin templates in the process.

This is a development tool. You should be familiar with Plone and buildout to
use it.

.. warning::
   This package is compatible with ``ZopeSkel < 3.0`` only.
   
Usage
^^^^^

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

.. _vs-zopeskel-diazo:

vs.zopeskel.diazo
-----------------

The `vs.zopeskel.diazo v1.0`_ package contains the following :ref:`ZopeSkel <zopeskel>` templates:


bootstrap
^^^^^^^^^

A :ref:`ZopeSkel <zopeskel>` template which allows individual adaptations of the 
:ref:`Bootstrap CSS framework <bootstrap-css-framework>` theme. Therefore it uses 
:ref:`z3c.jbot <z3c-jbot>` to overwrite existing templates with 
:ref:`z3c.jbot <z3c-jbot>`.

Also, you should use :ref:`LESS <less>` variables, mixins, etc. Therefore, the
`Buildout <http://www.buildout.org/>`_ configuration file will also install
`Bower <https://bower.io/>`_ and `Grunt <http://gruntjs.com/>`_ to recompile the
bootstrap :ref:`LESS <less>` files.

Usage
`````

For use the ``bootstrap`` :ref:`ZopeSkel <zopeskel>` template, execute the follow command 
and response the questions in the standard input from the console command:

::

    $ cd src/ && ../bin/zopeskel bootstrap my.theme

This will create a Python package with a directory structure like this:

::

    my.theme
    ├── bootstrap.py
    ├── buildout.cfg
    ├── docs
    │   ├── INSTALL.txt
    │   ├── LICENSE.GPL
    │   └── LICENSE.txt
    ├── my
    │   └── theme
    │       ├── configure.zcml
    │       ├── diazo_resources
    │       │   ├── favicon.ico
    │       │   ├── img
    │       │   │   ├── apple-touch-icon-144x144-precomposed.png
    │       │   │   ├── apple-touch-icon-57x57-precomposed.png
    │       │   │   ├── apple-touch-icon-72x72-precomposed.png
    │       │   │   ├── apple-touch-icon.png
    │       │   │   └── apple-touch-icon-precomposed.png
    │       │   ├── index.html
    │       │   ├── manifest.cfg
    │       │   ├── preview.png
    │       │   ├── rules.xml
    │       │   └── static
    │       │       ├── css
    │       │       │   └── main.css
    │       │       ├── fonts
    │       │       ├── img
    │       │       └── js
    │       │           └── main.js
    │       ├── Gruntfile.js
    │       ├── interfaces.py
    │       ├── locales
    │       ├── overrides
    │       │   └── plone.app.layout.viewlets.footer.pt
    │       ├── profiles
    │       │   └── default
    │       │       ├── browserlayer.xml
    │       │       ├── cssregistry.xml
    │       │       ├── jsregistry.xml
    │       │       ├── metadata.xml
    │       │       └── theme.xml
    │       └── version.txt
    ├── setup.cfg
    └── setup.py

----

.. _toutpt-zopeskel:

toutpt.zopeskel
---------------

The `toutpt.zopeskel v1.3.3`_ package provide new templates for :ref:`ZopeSkel <zopeskel>` 
2.X package. The package contains the following templates:


toutpt_diazo960
^^^^^^^^^^^^^^^

Create a Plone theme using ``plone.app.theming`` package. The theme is pure Diazo theme 
using 960 css.

The package profile install the theme, activate it, and unactivate ``column.css`` file
(aka deco). It loads all resources in corresponding registry.

Usage
`````

For use the ``toutpt_diazo960`` :ref:`ZopeSkel <zopeskel>` template, execute the follow command 
and response the questions in the standard input from the console command:

::

    $ cd src/ && ../bin/zopeskel toutpt_diazo960 my.diazotheme960

This will create a Python package with a directory structure like this:

::

    my.diazotheme960/
    ├── bootstrap.py
    ├── buildout.cfg
    ├── docs
    │   ├── HISTORY.txt
    │   ├── INSTALL.txt
    │   ├── LICENSE.GPL
    │   └── LICENSE.txt
    ├── MANIFEST.in
    ├── my
    │   ├── diazotheme960
    │   │   ├── configure.zcml
    │   │   ├── __init__.py
    │   │   ├── profiles
    │   │   │   └── default
    │   │   │       ├── cssregistry.xml
    │   │   │       ├── jsregistry.xml
    │   │   │       ├── metadata.xml
    │   │   │       └── theme.xml
    │   │   ├── static
    │   │   │   ├── css
    │   │   │   │   ├── grid.css
    │   │   │   │   └── theme.css
    │   │   │   ├── images
    │   │   │   │   └── logo.png
    │   │   │   ├── js
    │   │   │   │   └── theme.js
    │   │   │   ├── manifest.cfg
    │   │   │   ├── overrides
    │   │   │   │   └── plone.app.layout.viewlets.logo.pt
    │   │   │   ├── rules.xml
    │   │   │   ├── theme-one.html
    │   │   │   ├── theme-three.html
    │   │   │   ├── theme-two-left.html
    │   │   │   └── theme-two-right.html
    │   │   ├── tests.py
    │   │   ├── upgrades.py
    │   │   └── upgrades.zcml
    │   └── __init__.py
    ├── my.diazotheme960-configure.zcml
    ├── my.diazotheme960.egg-info
    │   ├── dependency_links.txt
    │   ├── entry_points.txt
    │   ├── namespace_packages.txt
    │   ├── not-zip-safe
    │   ├── PKG-INFO
    │   ├── requires.txt
    │   ├── SOURCES.txt
    │   └── top_level.txt
    ├── README.rst
    └── setup.py


toutpt_diazobootstrap
^^^^^^^^^^^^^^^^^^^^^

Create a Plone theme using ``plone.app.theming`` package. The theme is pure Diazo theme 
using Twitter's :ref:`Bootstrap Grid <bootstrap-css-framework>` (responsive mode).

The package profile install the theme, activate it, and unactivate ``column.css`` file
(aka deco) and ``mobile.css`` file. It loads all resources in corresponding registry
and override the 'main_template' to reset the viewport.

Usage
`````

For use the ``toutpt_diazobootstrap`` :ref:`ZopeSkel <zopeskel>` template, execute the follow command 
and response the questions in the standard input from the console command:

::

    $ cd src/ && ../bin/zopeskel toutpt_diazobootstrap my.diazobootstrap

This will create a Python package with a directory structure like this:

::

    my.diazobootstrap/
    ├── bootstrap.py
    ├── buildout.cfg
    ├── docs
    │   ├── HISTORY.txt
    │   ├── INSTALL.txt
    │   ├── LICENSE.GPL
    │   └── LICENSE.txt
    ├── MANIFEST.in
    ├── my
    │   ├── diazobootstrap
    │   │   ├── configure.zcml
    │   │   ├── __init__.py
    │   │   ├── profiles
    │   │   │   └── default
    │   │   │       ├── cssregistry.xml
    │   │   │       ├── jsregistry.xml
    │   │   │       ├── metadata.xml
    │   │   │       ├── skins.xml
    │   │   │       └── theme.xml
    │   │   ├── skins
    │   │   │   └── my_diazobootstrap_custom
    │   │   │       └── main_template.pt
    │   │   ├── static
    │   │   │   ├── css
    │   │   │   │   ├── grid.less
    │   │   │   │   ├── layouts.less
    │   │   │   │   ├── mixins.less
    │   │   │   │   ├── reset.less
    │   │   │   │   ├── responsive.less
    │   │   │   │   ├── scaffolding.less
    │   │   │   │   ├── theme.css
    │   │   │   │   ├── theme.less
    │   │   │   │   ├── theme-variables.less
    │   │   │   │   └── variables.less
    │   │   │   ├── images
    │   │   │   │   └── logo.png
    │   │   │   ├── js
    │   │   │   │   └── theme.js
    │   │   │   ├── manifest.cfg
    │   │   │   ├── overrides
    │   │   │   │   └── plone.app.layout.viewlets.logo.pt
    │   │   │   ├── rules.xml
    │   │   │   ├── theme-one.html
    │   │   │   ├── theme-three.html
    │   │   │   ├── theme-two-left.html
    │   │   │   └── theme-two-right.html
    │   │   ├── tests.py
    │   │   ├── upgrades.py
    │   │   └── upgrades.zcml
    │   └── __init__.py
    ├── my.diazobootstrap-configure.zcml
    ├── my.diazobootstrap.egg-info
    │   ├── dependency_links.txt
    │   ├── entry_points.txt
    │   ├── namespace_packages.txt
    │   ├── not-zip-safe
    │   ├── PKG-INFO
    │   ├── requires.txt
    │   ├── SOURCES.txt
    │   └── top_level.txt
    ├── README.rst
    └── setup.py


toutpt_collectivejs
^^^^^^^^^^^^^^^^^^^

Create a package to provide a javascript library to Plone. Many ``collective.js.*`` 
packages can be found like jquery.ui.

This template has been used to create ``collective.js.formalize`` package.

Usage
`````

For use the ``toutpt_collectivejs`` :ref:`ZopeSkel <zopeskel>` template, execute the follow command 
and response the questions in the standard input from the console command:

::

    $ cd src/ && ../bin/zopeskel toutpt_collectivejs collective.js.myjavascripts

This will create a Python package with a directory structure like this:

::

    collective.js.myjavascripts/
    ├── bootstrap.py
    ├── buildout.cfg
    ├── collective
    │   ├── __init__.py
    │   └── js
    │       ├── __init__.py
    │       └── myjavascripts
    │           ├── configure.zcml
    │           ├── __init__.py
    │           ├── interfaces.py
    │           ├── profiles
    │           │   └── default
    │           │       ├── browserlayer.xml
    │           │       ├── cssregistry.xml
    │           │       ├── jsregistry.xml
    │           │       └── metadata.xml
    │           └── upgrades
    │               ├── configure.zcml
    │               ├── __init__.py
    │               └── v1000_to_1001.py
    ├── collective.js.myjavascripts.egg-info
    │   ├── dependency_links.txt
    │   ├── entry_points.txt
    │   ├── namespace_packages.txt
    │   ├── not-zip-safe
    │   ├── PKG-INFO
    │   ├── requires.txt
    │   ├── SOURCES.txt
    │   └── top_level.txt
    ├── docs
    │   └── HISTORY.txt
    ├── MANIFEST.in
    ├── README.rst
    └── setup.py


toutpt_collective
^^^^^^^^^^^^^^^^^

Create a package to be a collective add-on. It will provides tests using 
``plone.app.testing`` package, upgrades for *GenericSetup* and a *Browser layer*. 
All common needs are their.

Usage
`````

For use the ``toutpt_collective`` :ref:`ZopeSkel <zopeskel>` template, execute the follow command 
and response the questions in the standard input from the console command:

::

    $ cd src/ && ../bin/zopeskel toutpt_collective collective.mypackage

This will create a Python package with a directory structure like this:

::

    collective.mypackage/
    ├── bootstrap.py
    ├── buildout.cfg
    ├── collective
    │   ├── __init__.py
    │   └── mypackage
    │       ├── browser
    │       │   ├── configure.zcml
    │       │   ├── __init__.py
    │       │   └── interfaces.py
    │       ├── configure.zcml
    │       ├── __init__.py
    │       ├── locales
    │       │   ├── collective.mypackage.pot
    │       │   ├── en
    │       │   │   └── LC_MESSAGES
    │       │   │       └── collective.mypackage.po
    │       │   └── fr
    │       │       └── LC_MESSAGES
    │       │           └── collective.mypackage.po
    │       ├── profiles
    │       │   └── default
    │       │       ├── browserlayer.xml
    │       │       └── metadata.xml
    │       ├── rebuild_i18n.sh
    │       ├── testing.py
    │       ├── tests
    │       │   ├── base.py
    │       │   ├── __init__.py
    │       │   └── test_setup.py
    │       └── upgrades
    │           ├── configure.zcml
    │           ├── __init__.py
    │           └── v1x.py
    ├── collective.mypackage-configure.zcml
    ├── collective.mypackage.egg-info
    │   ├── dependency_links.txt
    │   ├── entry_points.txt
    │   ├── namespace_packages.txt
    │   ├── not-zip-safe
    │   ├── PKG-INFO
    │   ├── requires.txt
    │   ├── SOURCES.txt
    │   └── top_level.txt
    ├── docs
    │   └── HISTORY.txt
    ├── MANIFEST.in
    ├── README.rst
    └── setup.py

.. _`ZopeSkel v2.21.2`: https://pypi.org/project/ZopeSkel/2.21.2/
.. _`PasteScript v1.7.5`: https://pypi.org/project/PasteScript/1.7.5/
.. _`plone.app.theming`: https://pypi.org/project/plone.app.theming/1.1.8/
.. _`zopeskel.diazochildtheme v0.1`: https://pypi.org/project/zopeskel.diazochildtheme/0.1/
.. _`diazotheme.frameworks`: https://github.com/collective/diazotheme.frameworks
.. _`zopeskel.diazotheme v1.1`: https://pypi.org/project/zopeskel.diazotheme/1.1/
.. _`vs.zopeskel.diazo v1.0`: https://pypi.org/project/vs.zopeskel.diazo/1.0/
.. _`toutpt.zopeskel v1.3.3`: https://pypi.org/project/toutpt.zopeskel/1.3.3/
.. _`z3c.jbot`: https://pypi.org/project/z3c.jbot/
