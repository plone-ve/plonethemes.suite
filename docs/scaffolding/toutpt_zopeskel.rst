.. _toutpt-zopeskel:

toutpt.zopeskel
---------------

The `toutpt.zopeskel v1.3.3`_ package provide new templates for :ref:`ZopeSkel <zopeskel>` 
2.X package. 

.. note::
    This is a development tool. You should be familiar with Plone and buildout to
    use it.

The ``toutpt.zopeskel`` package contains the following templates:


toutpt_diazo960
^^^^^^^^^^^^^^^

Create a Plone theme using `plone.app.theming`_ package. The theme is pure Diazo theme 
using 960 css.

The package profile install the theme, activate it, and unactivate ``column.css`` file
(aka deco). It loads all resources in corresponding registry.

Usage
`````

For use the ``toutpt_diazo960`` :ref:`ZopeSkel <zopeskel>` template, execute the follow 
command and response the questions in the standard input from the console command:

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


----


toutpt_diazobootstrap
^^^^^^^^^^^^^^^^^^^^^

Create a Plone theme using `plone.app.theming`_ package. The theme is pure Diazo theme 
using Twitter's :ref:`Bootstrap Grid <bootstrap-css-framework>` (responsive mode).

The package profile install the theme, activate it, and unactivate ``column.css`` file
(aka deco) and ``mobile.css`` file. It loads all resources in corresponding registry
and override the 'main_template' to reset the viewport.

Usage
`````

For use the ``toutpt_diazobootstrap`` :ref:`ZopeSkel <zopeskel>` template, execute the 
follow command and response the questions in the standard input from the console command:

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


----


toutpt_collectivejs
^^^^^^^^^^^^^^^^^^^

Create a package to provide a javascript library to Plone. Many ``collective.js.*`` 
packages can be found like :ref:`jquery.ui <jquery-ui-library>`.

This template has been used to create ``collective.js.formalize`` package.

Usage
`````

For use the ``toutpt_collectivejs`` :ref:`ZopeSkel <zopeskel>` template, execute the 
follow command and response the questions in the standard input from the console command:

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

Examples
````````

Here some examples about ``collective.js.*`` packages:

- :ref:`collective.js.bootstrap <collective-js-bootstrap>`

- :ref:`collective.js.galleria <collective-js-galleria>`

- :ref:`collective.js.supersized <collective-js-supersized>`

- Others ``collective.js.*`` packages are available on `GitHub.com`_

----


toutpt_collective
^^^^^^^^^^^^^^^^^

Create a package to be a collective add-on. It will provides tests using 
``plone.app.testing`` package, upgrades for *GenericSetup* and a *Browser layer*. 
All common needs are their.

Usage
`````

For use the ``toutpt_collective`` :ref:`ZopeSkel <zopeskel>` template, execute the 
follow command and response the questions in the standard input from the console command:

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


----

.. _`plone.app.theming`: https://pypi.org/project/plone.app.theming/1.1.8/
.. _`toutpt.zopeskel v1.3.3`: https://pypi.org/project/toutpt.zopeskel/1.3.3/
.. _`GitHub.com`: https://github.com/search?q=collective.js.*&ref=opensearch
