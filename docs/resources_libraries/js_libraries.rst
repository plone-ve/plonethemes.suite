.. _javascript-libraries:

Javascript libraries
====================

The **"Plone theming suite"** includes the following *Javascript* libraries as js resources 
or bundle of static files supported:


.. _collective-js-bootstrap:

collective.js.bootstrap
-----------------------

The `collective.js.bootstrap`_ package provide :ref:`Twitter Bootstrap CSS framework <bootstrap-css-framework>` v2.3.1 as browser 
resources in Plone.

The *Twitter Bootstrap* Resources are the following:

::

  ++resource++collective.js.bootstrap/
  ++resource++collective.js.bootstrap/js/bootstrap.js
  ++resource++collective.js.bootstrap/js/bootstrap.min.js
  ++resource++collective.js.bootstrap/css/bootstrap.css
  ++resource++collective.js.bootstrap/css/bootstrap.min.css
  ++resource++collective.js.bootstrap/css/bootstrap-responsive.css
  ++resource++collective.js.bootstrap/css/bootstrap-responsive.min.css
  ++resource++collective.js.bootstrap/img/glyphicons-halflings.png
  ++resource++collective.js.bootstrap/img/glyphicons-halflings-white.png


.. note::
    Please, checkout more information about :ref:`Twitter Bootstrap CSS framework <bootstrap-css-framework>`

How to install
^^^^^^^^^^^^^^

This add-on just need to be present in the zope instance. No profile to apply.


.. _collective-js-galleria:

collective.js.galleria
----------------------

The `collective.js.galleria`_ package register `Galleria`_ :ref:`jQuery <jquery-library>` 
plugin 1.2.9 2013-01-10 version in Plone's resource registries.

The *Galleria* Resources are the following:

::

  ++resource++collective.js.galleria/
  ++resource++collective.js.galleria/images/classic-loader.gif
  ++resource++collective.js.galleria/images/classic-map.png
  ++resource++collective.js.galleria/galleria.classic.css
  ++resource++collective.js.galleria/galleria.classic.js
  ++resource++collective.js.galleria/galleria.js
  ++resource++collective.js.galleria/plugins/flickr/flickr-demo.html
  ++resource++collective.js.galleria/plugins/flickr/flickr-loader.gif
  ++resource++collective.js.galleria/plugins/flickr/galleria.flickr.js
  ++resource++collective.js.galleria/plugins/flickr/galleria.flickr.min.js
  ++resource++collective.js.galleria/plugins/flickr/loader.gif
  ++resource++collective.js.galleria/plugins/history/galleria.history.js
  ++resource++collective.js.galleria/plugins/history/galleria.history.min.js
  ++resource++collective.js.galleria/plugins/history/history-demo.html
  ++resource++collective.js.galleria/plugins/picasa/galleria.picasa.js
  ++resource++collective.js.galleria/plugins/picasa/galleria.picasa.min.js
  ++resource++collective.js.galleria/plugins/picasa/picasa-demo.html
  ++resource++collective.js.galleria/plugins/picasa/loader.gif


About Galleria
^^^^^^^^^^^^^^

``Galleria`` is a JavaScript image gallery framework built on top of the :ref:`jQuery <jquery-library>`
library. The aim is to simplify the process of creating professional image
galleries for the web and mobile devices.

How to install
^^^^^^^^^^^^^^

This add-on can be installed as any other Plone add-on. Please follow official 
`install add-ons documentation`_.

.. _`install add-ons documentation`: https://docs.plone.org/4/en/adapt-and-extend/install_add_ons.html

Notes
^^^^^

``Galleria`` in its way to manage theme parse all link tags to find the css attached
to the theme. To make it work in production mode you must add themes javascript
and css called by the template.

::

    // look for manually added CSS
    $('link').each(function( i, link ) {
        reg = new RegExp( theme.css.replace('\+\+resource\+\+','\\+\\+resource\\+\\+') );
        if ( reg.test( link.href ) ) {
            // we found the css
            css = true;
            Galleria.theme = theme;
            return false;
        }
    });

As you can see the original code has been patched to support ``++resource++`` url.


.. _collective-js-supersized:

collective.js.supersized
------------------------

The `collective.js.supersized`_ package add integration of the :ref:`jQuery <jquery-library>` 
Supersized v3.2.7 in Plone 4 (tested) and Plone 3 (untested). There is a small change from 
the original ``supersized.shutter.js`` (the image path), and a few in the css files.

.. warning::
    This product is no longer used for :ref:`collective.plonetruegallery <plonetruegallery>` 
    package, use the :ref:`collective.ptg.supersized <collective-ptg-supersized>` package instead

News item view
^^^^^^^^^^^^^^

You can see the "single background image mode" by 

- installing the product
- go to ``http://mysite/mynewsitemwithimage/@@supersized_view``


Dexterity behavior
^^^^^^^^^^^^^^^^^^

Version 0.4 added a dexterity behavior.
- Add one or more image fields to your content type... or
- Add lead image behavior to your content type
- If you add several image fields, you will get a slideshow


Example on Using it on folders
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- add a folderish content type (lets call it «Myfoldertype» with a image field 
  named «Image» (or content lead image)
- Add a content type («mytype») with supersized behavior
- Add a «Myfoldertype» to your site
- Add a «mytype» in «Myfoldertype» and you will get the image from «Myfoldertype» 
  supersized 


Gallery effect
^^^^^^^^^^^^^^

If you add more than one image to your content type, you will get a slideshow effect.
It will only work for images on the same content, not its parent


The control panel
^^^^^^^^^^^^^^^^^

In the (medialog) control panel, you can choose which size to use for the background 
image and a few other settings.


.. _`collective.js.bootstrap`: https://github.com/collective/collective.js.bootstrap
.. _`collective.js.galleria`: https://pypi.org/project/collective.js.galleria
.. _`Galleria`: http://galleria.io
.. _`collective.js.supersized`: https://github.com/collective/collective.js.supersized

.. _`collective.js.simplecart`: https://github.com/collective/collective.js.simplecart
.. _`collective.js.nivoslider`: https://github.com/espenmn/collective.js.nivoslider
.. _`collective.js.oembed`: https://github.com/collective/collective.js.oembed
.. _`collective.js.speakjs`: https://github.com/collective/collective.js.speakjs
.. _`collective.js.jstree`: https://github.com/collective/collective.jstree
