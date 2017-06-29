Strings library
=============================================
.. highlight:: lua

Reference from `lua manual <https://www.lua.org/manual/5.0/manual.html#5.3>`_

#############
Functions
#############

============
dump
============

Returns a binary representation of the given function, so that a later loadstring on that string returns a copy of the function. Function must be a Lua function without upvalues::

    string.dump(fn)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``function`` fn
    lua function

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``string`` result

============
char
============

Receives 0 or more integers. Returns a string with length equal to the number of arguments, in which each character has the internal numerical code equal to its correspondent argument::

    string.char(...)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``number`` ...
    integers

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``string`` result

============
byte
============

Returns the internal numerical code of the i-th character of s, or nil if the index is out of range. If i is absent, then it is assumed to be 1. i may be negative::

    string.byte(s [, i])

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``string`` s

* ``number`` i

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``number`` result

============
unicode
============

TODO

============
len
============

Returns the length of a string::

    string.len(str)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``string`` str

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``number`` result

============
match
============

TODO

============
gmatch
============

TODO

============
gsub
============

TODO

============
find
============

TODO

============
lower
============

TODO

============
upper
============

TODO

============
rep
============

TODO

============
format
============

TODO

============
reverse
============

TODO

============
sub
============

TODO

============
startsWith
============

TODO

============
endsWith
============

TODO

============
contains
============

TODO
