.. _behaviors-themes:


Behaviors Themes
================

The **"Plone theming suite"** includes the following behaviors themes supported:


Local Diazo Theme
-----------------

The `collective.behavior.localdiazo`_ package adds Dexterity behavior to enable a 
local :ref:`Diazo theme <diazo-themes>`. for Plone.

In Plone's control panel go to :guilabel:`Dexterity Content Types`, select your 
content type, go to the :guilabel:`Behaviors` tab and enable the :guilabel:`Local registry` 
and :guilabel:`Local Diazo theme` behaviors.

.. figure:: ../../_static/collective_behavior_localdiazo_00.png
  :align: center
  :width: 75%
  :alt: Behaviors editor for "collective.behavior.localdiazo"

  Behaviors editor for *collective.behavior.localdiazo*.

Add a new object; you will see a new field called :guilabel:`Theme` and select a 
Diazo theme from the list.

.. figure:: ../../_static/collective_behavior_localdiazo_01.png
  :align: center
  :width: 75%
  :alt: Adding a Microsite content type

  Adding a Microsite content type.

Now when you access your container you will see the Diazo theme applied to it.

.. figure:: ../../_static/collective_behavior_localdiazo_02.png
  :align: center
  :width: 75%
  :alt: A local behavior of Diazo theme for Microsite

  A local behavior of Diazo theme for Microsite.

If you followed all the instructions and the theme is not applied, make sure Diazo 
theming is enabled on :guilabel:`Theme settings`.

.. figure:: ../../_static/collective_behavior_localdiazo_03.png
  :align: center
  :width: 75%
  :alt: The theme settings for Microsite

  The theme settings for Microsite.

----

Local Skin Theme
----------------

The `collective.behavior.localskin`_ package adds Dexterity behavior to enable a local 
:ref:`theme skin <plone-theme-skins>` for Plone.

In Plone's control panel go to :guilabel:`Dexterity Content Types`, select your content 
type, go to the :guilabel:`Behaviors` tab and enable the :guilabel:`Local registry` and 
:guilabel:`Local skin theme` behaviors.

.. figure:: ../../_static/collective_behavior_localskin_00.png
  :align: center
  :width: 75%
  :alt: Behaviors editor for "collective.behavior.localskin"

  Behaviors editor for *collective.behavior.localskin*.

Add a new object; now when you access your container created.

.. figure:: ../../_static/collective_behavior_localskin_01.png
  :align: center
  :width: 75%
  :alt: Adding a Microsite content type

  Adding a Microsite content type.

Later edit the object created; you will see a new field called :guilabel:`Skin name` and 
select a skin theme from the list.

.. figure:: ../../_static/collective_behavior_localskin_02.png
  :align: center
  :width: 75%
  :alt: Editing a Microsite and select "Skin name" theme

  Editing a Microsite and select ``Skin name`` theme.

Now when you access your container you will see the Skin theme applied to it.

.. figure:: ../../_static/collective_behavior_localskin_03.png
  :align: center
  :width: 75%
  :alt: A local behavior of Skin theme for Microsite

  A local behavior of Skin theme for Microsite.

.. _`collective.behavior.localdiazo`: https://pypi.org/project/collective.behavior.localdiazo
.. _`collective.behavior.localskin`: https://pypi.org/project/collective.behavior.localskin
