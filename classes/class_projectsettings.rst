.. Generated automatically by doc/tools/makerst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the ProjectSettings.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_ProjectSettings:

ProjectSettings
===============

**Inherits:** :ref:`Object<class_object>`

**Category:** Core

Brief Description
-----------------

Contains global variables accessible from everywhere.

Member Functions
----------------

+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| void                           | :ref:`add_property_info<class_ProjectSettings_add_property_info>` **(** :ref:`Dictionary<class_dictionary>` hint **)**                              |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| void                           | :ref:`clear<class_ProjectSettings_clear>` **(** :ref:`String<class_string>` name **)**                                                              |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`          | :ref:`get_order<class_ProjectSettings_get_order>` **(** :ref:`String<class_string>` name **)** const                                                |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Variant<class_variant>`  | :ref:`get_setting<class_ProjectSettings_get_setting>` **(** :ref:`String<class_string>` name **)** const                                            |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`String<class_string>`    | :ref:`globalize_path<class_ProjectSettings_globalize_path>` **(** :ref:`String<class_string>` path **)** const                                      |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`        | :ref:`has_setting<class_ProjectSettings_has_setting>` **(** :ref:`String<class_string>` name **)** const                                            |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`        | :ref:`load_resource_pack<class_ProjectSettings_load_resource_pack>` **(** :ref:`String<class_string>` pack **)**                                    |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`String<class_string>`    | :ref:`localize_path<class_ProjectSettings_localize_path>` **(** :ref:`String<class_string>` path **)** const                                        |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`        | :ref:`property_can_revert<class_ProjectSettings_property_can_revert>` **(** :ref:`String<class_string>` name **)**                                  |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Variant<class_variant>`  | :ref:`property_get_revert<class_ProjectSettings_property_get_revert>` **(** :ref:`String<class_string>` name **)**                                  |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`          | :ref:`save<class_ProjectSettings_save>` **(** **)**                                                                                                 |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`          | :ref:`save_custom<class_ProjectSettings_save_custom>` **(** :ref:`String<class_string>` file **)**                                                  |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| void                           | :ref:`set_initial_value<class_ProjectSettings_set_initial_value>` **(** :ref:`String<class_string>` name, :ref:`Variant<class_variant>` value **)** |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| void                           | :ref:`set_order<class_ProjectSettings_set_order>` **(** :ref:`String<class_string>` name, :ref:`int<class_int>` position **)**                      |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| void                           | :ref:`set_setting<class_ProjectSettings_set_setting>` **(** :ref:`String<class_string>` name, :ref:`Variant<class_variant>` value **)**             |
+--------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+

Description
-----------

Contains global variables accessible from everywhere. Use "ProjectSettings.get_setting(variable)", "ProjectSettings.set_setting(variable,value)" or "ProjectSettings.has_setting(variable)" to access them. Variables stored in project.godot are also loaded into ProjectSettings, making this object very useful for reading custom game configuration options.

Member Function Description
---------------------------

.. _class_ProjectSettings_add_property_info:

- void **add_property_info** **(** :ref:`Dictionary<class_dictionary>` hint **)**

Add a custom property info to a property. The dictionary must contain: name::ref:`String<class_string>`(the name of the property) and type::ref:`int<class_int>`(see TYPE\_\* in :ref:`@GlobalScope<class_@globalscope>`), and optionally hint::ref:`int<class_int>`(see PROPERTY_HINT\_\* in :ref:`@GlobalScope<class_@globalscope>`), hint_string::ref:`String<class_string>`.

Example:

::

    ProjectSettings.set("category/property_name", 0)
    
    var property_info = {
        "name": "category/property_name",
        "type": TYPE_INT,
        "hint": PROPERTY_HINT_ENUM,
        "hint_string": "one,two,three"
    }
    
    ProjectSettings.add_property_info(property_info)

.. _class_ProjectSettings_clear:

- void **clear** **(** :ref:`String<class_string>` name **)**

Clear the whole configuration (not recommended, may break things).

.. _class_ProjectSettings_get_order:

- :ref:`int<class_int>` **get_order** **(** :ref:`String<class_string>` name **)** const

Return the order of a configuration value (influences when saved to the config file).

.. _class_ProjectSettings_get_setting:

- :ref:`Variant<class_variant>` **get_setting** **(** :ref:`String<class_string>` name **)** const

.. _class_ProjectSettings_globalize_path:

- :ref:`String<class_string>` **globalize_path** **(** :ref:`String<class_string>` path **)** const

Convert a localized path (res://) to a full native OS path.

.. _class_ProjectSettings_has_setting:

- :ref:`bool<class_bool>` **has_setting** **(** :ref:`String<class_string>` name **)** const

Return true if a configuration value is present.

.. _class_ProjectSettings_load_resource_pack:

- :ref:`bool<class_bool>` **load_resource_pack** **(** :ref:`String<class_string>` pack **)**

.. _class_ProjectSettings_localize_path:

- :ref:`String<class_string>` **localize_path** **(** :ref:`String<class_string>` path **)** const

Convert a path to a localized path (res:// path).

.. _class_ProjectSettings_property_can_revert:

- :ref:`bool<class_bool>` **property_can_revert** **(** :ref:`String<class_string>` name **)**

.. _class_ProjectSettings_property_get_revert:

- :ref:`Variant<class_variant>` **property_get_revert** **(** :ref:`String<class_string>` name **)**

.. _class_ProjectSettings_save:

- :ref:`int<class_int>` **save** **(** **)**

.. _class_ProjectSettings_save_custom:

- :ref:`int<class_int>` **save_custom** **(** :ref:`String<class_string>` file **)**

.. _class_ProjectSettings_set_initial_value:

- void **set_initial_value** **(** :ref:`String<class_string>` name, :ref:`Variant<class_variant>` value **)**

.. _class_ProjectSettings_set_order:

- void **set_order** **(** :ref:`String<class_string>` name, :ref:`int<class_int>` position **)**

Set the order of a configuration value (influences when saved to the config file).

.. _class_ProjectSettings_set_setting:

- void **set_setting** **(** :ref:`String<class_string>` name, :ref:`Variant<class_variant>` value **)**


