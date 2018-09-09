.. _collective-easyslider:

Easy Slider
-----------

The `collective.easyslider <https://github.com/collective/collective.easyslider>`_ product 
will allow you to apply an ``easySlider`` to any page with the ability to create each slide using 
a WYSIWYG editor. It also provides a slider view for ``Folders`` and ``Collections``.

.. note::
    This package allows you to easily add an ``easySlider`` content rotator to any page 
    on a Plone site using a WYSIWYG editor to design each slide.


How It Works
^^^^^^^^^^^^^

On a page, click actions -> :guilabel:`Add new...` dropdown menu :guilabel:`Slider`.  
It should bring you to a slider settings page where you can modify different aspects 
of the slider and add/remove slides using a WYSWGY editor.
Keep in mind that the slides are fixed width so you need to specify the size you want. 
Then you'll want to start adding your slides.  To do this just click ``add new slide`` 
near the bottom of the page.  Once you've finished adding slides and re-ordering slides, 
click ``save`` and you should see the slider on your page now.

You can also select a slider view for Folder and Collection content types. Then the 
slider settings for that page will include settings to limit the amount of slides to 
have and to limit the type of slides used.


Easy Template Integration
^^^^^^^^^^^^^^^^^^^^^^^^^^

If you'd like to add dynamic content to your slides, add :ref:`collective.easytemplate <collective-easytemplate>`
to your eggs section in buildout, re-run buildout and restart your installation.
Then in the slider settings make sure you enable Easy Template.

You can also render sliders in a Easy Template. The syntax is:

::

    {{ slider("../front-page") }}


And for the sliderview:

::

    {{ sliderview("../a-collection") }}


Rendering Slider in Templates
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can also easily render your slider in a page template if you'd like even more 
control over how it is displayed:

::

    <tal:slider tal:content="structure context/../front-page/@@slider_util/render_inline" />

And for the sliderview:

::

    <tal:slider tal:content="structure context/../front-page/@@slider_util/render_sliderview_inline" />

.. todo:: TODO finish this section


----

.. _collective-easytemplate:

Easy Template
`````````````

The `collective.easytemplate <https://github.com/collective/collective.easytemplate>`_ 
package let you Dynamic HTML generation and scripting of pages, content rules, portlets 
and emails.

*Easy Template* (aka ``collective.easytemplate``) product brings easy dynamic texts to Plone. 
You don't need to create full blown product just for few dynamic pages any more - the 
most simplest things can be typed straight from the visual editor.

Templating is a way to add simple programming logic to text output. This product adds or enhances templating supports on various parts of Plone site.

Use cases
~~~~~~~~~

Possible use cases are e.g.

* Use unfiltered HTML on page body (``<script>`` et. al)

* Adding dynamic listings and tables on pages, like news listing

* Adding dynamic email bodies, titles and receivers in content rules actions

* Adding generated content to content rule action emails

* Show different text to logged in and anonymous users

* Creating a simple text portlet dynamically


Example
~~~~~~~

The following example demonstrates how text in Templated Document edit mode gets 
translated to generated HTML snippet in the view mode.

You write in WYSIWYG editor:

::

  Hello user!
  
  Please select one course from below:
  
  {{ list_folder("courses") }}

will result to the output:

::

  Hello user!
  
  Please select one course from below:
  
  * `Math <http://example.example>`_
  
  * `Marketing <http://example.example>`_
  
  * `Chemistry <http://example.example>`_

.. note::
    `More information and examples <http://opensourcehacker.com/2009/07/30/putting-views-like-sitemap-into-plone-content-tree-using-easy-template-add-on/>`_.


Security notice
~~~~~~~~~~~~~~~

Because ``collective.easytemplate`` allows entering unsafe HTML, like ``<script>`` on the pages 
by default, its creation is limited to the users with ``Manager`` role. 

.. todo:: TODO write this section
