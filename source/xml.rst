XML library
=======================
.. highlight:: lua

LuaConnector has built-in xml library

#############
Functions
#############

============
parse
============

Performs conversion from string with xml data to table::

    xml.parse(data)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``string`` data
    string with xml

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``table`` parsing result

Table structure is pretty simple. Every xml element has three fields:

* ``string`` name

* ``table`` attributes (key-value pair array)

* ``table`` child (array of child elements)

============
get
============

Helper function for getting data from xml table::

	xml.get(data, query)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``table`` data
    xml table from ``xml.parse``

* ``string`` query
	query string for getting xml

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``table``/``string`` requested data

=============
serialize
=============

TODO

################
Query language
################

Query language description for ``xml.get``

.. code-block:: lua

	local string = [[
	<?xml version="1.0" encoding="UTF-8"?>
	<settings>
		<graphics>
			<resolution ratio="1.65">1280x760</resolution>
			<shadows>23</shadows>
		</graphics>
		<sound></sound>
	</settings>
	]]

	local document = xml.parse(string)

	xml.get(document, "settings/graphics/resolution")    -- returns "1280x760"
	xml.get(document, "settings/graphics/resolution/!")  -- returns table with "resolution" element
	xml.get(document, "settings/graphics/1")             -- returns first element from "graphics" element
	xml.get(document, "settings/graphics/[2]")           -- returns first 2 elements from "graphics" element
	xml.get(document, "settings/graphics/resolution/[]") -- returns all attributes of "resolution"

#############
Examples
#############
