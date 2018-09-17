.. _vs-zopeskel-diazo:

vs.zopeskel.diazo
-----------------

The `vs.zopeskel.diazo v1.0`_ package contains the following :ref:`ZopeSkel <zopeskel>` templates:

.. note::
    This is a development tool. You should be familiar with Plone and buildout to
    use it.

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

.. _`vs.zopeskel.diazo v1.0`: https://pypi.org/project/vs.zopeskel.diazo/1.0/
