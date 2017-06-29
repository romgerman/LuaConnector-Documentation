JSON library
=============================================
.. highlight:: lua

MoonSharp has built-in json library and it's easy to use

.. code-block:: lua

	json.parse(jsonString)

Returns a table with the contents of the specified json string.

.. code-block:: lua

	json.serialize(table)

Returns a json string with the contents of the specified table.

.. code-block:: lua

	json.isNull(val)

Returns true if the value specified is a null read from a json

.. code-block:: lua

	json.null()

Returns a special value which is a representation of a null in a json
