.. _installation:

Quickstart
==========

Requirements
------------

First you need the follow system dependencies, please, execute follow the command: ::

    $ sudo apt-get update && sudo apt-get install git python-dev python-virtualenv

Download source code
--------------------

To get a copy the source code from git repository, execute follow the command: ::

    $ git clone https://github.com/plone-ve/plonethemes.suite.git

Development installation
------------------------

To get a basic development installation running follow the steps below: ::

    $ cd plonethemes.suite
    $ virtualenv .
    $ source ./bin/activate
    $ pip install -r requirements.txt
    $ buildout

..
        $ python bootstrap.py
        $ bin/buildout

Running the site
----------------

Once the buildout has finished, you can access the site by starting up Plone. ::

    $ RELOAD_PATH=src/ bin/instance fg

Then go to the site in your browser: http://localhost:8081/manage_main and log in with:

- :guilabel:`user`: admin
- :guilabel:`password`: admin

If you haven't already done so, you will have to create a Plone site by:

- click on the :guilabel:`Create a new Plone site` button
- you can leave all the default values in the form that appears
- scroll to the bottom of the page and click on the :guilabel:`Create Plone Site` button
