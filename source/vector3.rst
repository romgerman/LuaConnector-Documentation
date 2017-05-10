Vector3
=============================================
.. highlight:: lua

Vector3 class is almost identical to the class in GT-MP but contains a little more functions

To make a new instance of the class simply call ``Vector3(number, number, number)`` or ``Vector3:New(number, number, number)``

#############
Functions
#############

===============
Dot
===============

.. code-block:: lua

	Vector3:Dot(vector)

Returns dot product

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``Vector3`` vector
	a second vector

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``number``

===============
Cross
===============

.. code-block:: lua

	Vector3:Cross(vector)

Returns cross product

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``Vector3`` vector
	a second vector

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``Vector3``

===============
Length
===============

.. code-block:: lua

	Vector3:Length()

Returns length of a vector

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``Vector3``

===============
Normal
===============

.. code-block:: lua

	Vector3:Normal()

Returns normalized vector

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``Vector3``

===============
Normalize
===============

.. code-block:: lua

	Vector3:Normalize()

Normalizes a vector and returns itself

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``Vector3``

===============
DistanceTo
===============

.. code-block:: lua

	Vector3:DistanceTo(vector)

Returns a distance between two vectors

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``Vector3`` vector
	a second vector

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``number``

#############
Operators
#############

Following expressions can be used::

	v1 + v2    -- addition
	v1 - v2    -- subtraction
	v1 * num   -- multiplication by a number
	num * v1
	v1 / num   -- division by a number
	-v1        -- inversion
	v1 == v2   -- equality check
	v1 < v2    -- less than check
	v1 > v2
	v1 <= v2   -- less than or equal check
	v1 >= v2
