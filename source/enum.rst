Enum table helper functions
=============================================
.. highlight:: lua

=============
castTo
=============

Allows you to cast a number to an enum::

	Enum.castTo(enum, value)

---------
Arguments
---------

* ``Enum`` enum

* ``number`` value

----------
Example
----------

.. code-block:: lua

	local result = Enum.castTo(Enum.PedHash, -2109222095)
	print(result) -- output: Hipster01AFY

=============
value
=============

Use this function to get actual value::

	Enum.value(enum, ...)

---------
Arguments
---------

* all arguments should be in ``Enum`` type

----------
Example
----------

.. code-block:: lua

	print(Enum.value(Enum.PedHash.Chef2)) -- -2054645053
	print(Enum.value(Enum.PedHash.Chef2, Enum.PedHash.PrologueDriver)) -- output: -2054645053    -2057423197

