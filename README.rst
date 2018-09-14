Plone theming suite
====================

The idea of this buildout configuration is to install the latest version 
of Plone 4.3.x, along with many Plone theme skins, Diazo themes and useful 
theming tools for layout, custom icons and fonts and third-party theming 
add-ons.

This suite included the following:

* Scaffolding tools, included in this suite are 3 different packages.
* Plone theme skins, included in this suite are 7 different Plone theme skins add-on.
* Diazo themes, are included in this suite are over 50 different add-on.
* Some theming and layout tools.
* Some Web font tools.
* Some jQuery libraries.
* Severals CSS Frameworks with CSS and JS resources files.
* CSS Pre-Processing tools for LESS and SASS files.

**Note:**

  More information check out the suite full documentation http://plone-theming-suite.readthedocs.io/.

Development installation
------------------------

To get a basic development installation running follow the steps below: ::

    $ sudo apt-get update && sudo apt-get install git python-dev python-virtualenv
    $ git clone https://github.com/plone-ve/plonethemes.suite.git
    $ cd plonethemes.suite
    $ virtualenv .
    $ source ./bin/activate
    $ pip install -r requirements.txt
    $ python bootstrap.py
    $ bin/buildout

Running the site
----------------
Once the buildout has finished, you can access the site by starting up Plone. ::

    $ bin/instance fg

Then go to the site in your browser: http://localhost:8081/manage_main and log in with:

- user: admin
- password: admin

If you haven't already done so, you will have to create a Plone site by:

- click on the "Create a new Plone site" button
- you can leave all the default values in the form that appears
- scroll to the bottom of the page and click on the "Create Plone Site" button


Documentation installation
--------------------------

To get a local documentation copy follow the steps below: ::

    $ cd plonethemes.suite
    $ source ./bin/activate
    $ pip install -r requirements_docs.txt
    $ cd docs && make clean html

Support
=======

If you run into any issues trying to get this to work, please, add an
issue to the `tracker here`_ on this github project.


Collaborations
==============

Really thanks to:

Original Author
----------------

* Leonardo J .Caballero G. aka macagua

Impressive collaborations
-------------------------

* Eveli Ramirez aka Eveli

* Flamel Canto aka flamelcanto

* T\. Kim Nguyen aka tkimnguyen

* Full name aka username

For an updated list of all contributors visit the following URL: 
https://github.com/plone-ve/plonethemes.suite/graphs/contributors

.. _tracker here: https://github.com/plone-ve/plonethemes.suite/issues
