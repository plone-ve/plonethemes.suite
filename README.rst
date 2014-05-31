Plone theming suite
====================

The idea with this buildout configuration is 
show install a Plone latest version, with many 
Plone theme skins, Diazo Themes and usefull 
Theming tools for layout, adding custom icons 
and fonts with third-party add-ons theming into 
Plone.

Plone theme skins
------------------

In this suite are distributed around 6 differents
Plone theme skins.

- `quintagroup.theme.sunrain <https://github.com/quintagroup/quintagroup.theme.sunrain>`_.

- `quintagroup.theme.schools <https://github.com/quintagroup/quintagroup.theme.schools>`_.

- `quintagroup.theme.pythonreel <https://github.com/quintagroup/quintagroup.theme.pythonreel>`_.

- `plonetheme.aclark_twitter <https://github.com/collective/plonetheme.aclark_twitter>`_.

- `plonetheme.drupal <https://github.com/sylvainb/plonetheme.drupal>`_.

- `plonetheme.trantor <https://github.com/tristanlt/plonetheme.trantor>`_.

Diazo Themes
-------------

In this suite are distributed around 30 differents 
Generic Diazo themes.

- `plonetheme.amherst <https://github.com/collective/plonetheme.amherst>`_.

- `plonetheme.aqueouslight <https://github.com/collective/plonetheme.aqueouslight>`_.

- `plonetheme.armadillotec <https://github.com/macagua/plonetheme.armadillotec>`_.

- `plonetheme.bananaleaf <https://github.com/collective/plonetheme.bananaleaf>`_.

- `plonetheme.burned <https://github.com/collective/plonetheme.burned>`_.

- `plonetheme.codapress <https://github.com/collective/plonetheme.codapress>`_.

- `plonetheme.coolblue <https://github.com/collective/plonetheme.coolblue>`_.

- `plonetheme.darkened <https://github.com/collective/plonetheme.darkened>`_.

- `plonetheme.diazo_sunburst <https://github.com/aclark4life/plonetheme.diazo_sunburst>`_.

- `plonetheme.discovery <https://github.com/giacomos/plonetheme.discovery>`_.

- `plonetheme.earthlingtwo <http://svn.plone.org/svn/collective/plonetheme.earthlingtwo/trunk/>`_.

- `plonetheme.evergreen <https://github.com/giacomos/plonetheme.evergreen>`_.

- `plonetheme.flowerbuds <https://github.com/toutpt/plonetheme.flowerbuds>`_.

- `plonetheme.freshpick <https://github.com/collective/plonetheme.freshpick>`_.

- `plonetheme.gestured <https://github.com/dante1987/plonetheme.gestured>`_.

- `plonetheme.grungeera <https://github.com/collective/plonetheme.grungeera>`_.

- `plonetheme.keepitsimple <https://github.com/collective/plonetheme.keepitsimple>`_.

- `plonetheme.leavesdew <https://github.com/giacomos/plonetheme.leavesdew>`_.

- `plonetheme.motion <https://github.com/davilima6/plonetheme.motion>`_.

- `plonetheme.redmusic <https://github.com/giacomos/plonetheme.redmusic>`_.

- `plonetheme.pythonmexico <https://github.com/PythonMexico/plonetheme.pythonmexico>`_.

- `plonetheme.pollination <http://svn.plone.org/svn/collective/plonetheme.pollination/trunk/>`_.

- `plonetheme.plumigreen <https://github.com/garbas/plonetheme.plumigreen>`_.

- `plonetheme.unbound11 <https://github.com/a-pasquale/plonetheme.unbound11>`_.

- `plonetheme.unilluminated <https://github.com/collective/plonetheme.unilluminated>`_.

- `plonetheme.transition <https://github.com/gyst/plonetheme.transition>`_.

- `plonetheme.woodexperience <https://github.com/redomino/plonetheme.woodexperience>`_.

- `plonetheme.yoko <https://github.com/tisto/plonetheme.yoko>`_.

- `plonetheme.changecenter <https://github.com/a-pasquale/plonetheme.changecenter>`_.

- `plonetheme.unam <https://github.com/imatem/plonetheme.unam>`_.

- `plonetheme.zopeorg <https://github.com/d2m/plonetheme.zopeorg>`_.

Theming tools features
-----------------------

Plone theming suite includes some Plone products and 
configurations like these:

- `collective.cover <https://pypi.python.org/pypi/collective.cover>`_ 
  for edit to create front pages and other composite pages.

- `Products.Doormat <https://pypi.python.org/pypi/Products.Doormat>`_ 
  for adds a doormat viewlet and installs it in the Plone footer.

- `collective.fontawesome <https://pypi.python.org/pypi/collective.fontawesome>`_ 
  for add Font Awesome for Plone.

- `medialog.googlefonts <https://pypi.python.org/pypi/medialog.googlefonts>`_ 
  for add Googlefonts for Plone.
    

Development installation
------------------------

To get a basic development installation running 
follow the steps below: ::

    $ git clone https://github.com/plone-ve/plonethemes.suite.git
    $ cd plonethemes.suite
    $ python bootstrap.py
    $ bin/buildout -vvvvvvvvN

Running the site
----------------
Once the buildout has finished, you can access the site by starting up
Plone. ::

    $ bin/instance fg

Then go to the site in your browser: http://localhost:8080/Plone

The themes any aren't currently enabled, so you'll have to login to enable a theme for your Plone Site. ::

    username: admin
    password: admin

Others resources for Plone themes
---------------------------------

- `PloneThemes.org <http://plonethemes.org/>`_.

- `Beyondskins themes for Plone <http://www.beyondskins.com/>`_.

- `Beautiful Design and Powerful Plone Features <http://themes.quintagroup.com/>`_.

Reference
=========

- `Diazo themes revisited <http://blog.aclark.net/2012/09/24/diazo-themes-revisited/>`_.

- `"New" Plone theming has arrived <http://blog.aclark.net/2011/05/27/quotnewquot-plone-theming-has-arrived/>`_.

- `A report on plonetheme.* <http://blog.aclark.net/2010/11/04/a-report-on-plonetheme/>`_.