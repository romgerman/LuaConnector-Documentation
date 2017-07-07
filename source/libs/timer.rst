Timers library
================

Easy way to create and use timers. Timer's resolution depends on server's tick rate. So calculate min timer interval using ``1000/tickrate``.

#############
Functions
#############

============
create
============

Creates a new timer::

    timer.create(name, delay, repeat, callback)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``string`` name
    name of a timer. Can be ``nil``. Name should be unique

* ``number`` delay
    timer delay in milliseconds

* ``boolean`` repeat
    should timer repeat every ``delay`` ms or run only once

* ``function`` callback
    callback function that will fire on every tick

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``LuaTimer`` timer with methods ``start``, ``pause``, ``stop``, ``destroy``

============
get
============

Returns timer object by it's name::

    timer.get(name)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``string`` name
    name of a timer

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``LuaTimer`` or ``nil`` if not found

=============
start
=============

Starts a timer::

    timer.start(name)

^^^^^^^^^^^
Arguments
^^^^^^^^^^^

* ``string`` name
    name of a timer

============
pause
============

Pauses a timer::

    timer.pause(name)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``string`` name
    name of a timer

============
stop
============

Stops a timer::

    timer.stop(name)

^^^^^^^^^^^
Arguments
^^^^^^^^^^^

* ``string`` name
    name of a timer

============
destroy
============

Destroys a timer::

    timer.destroy(name)

^^^^^^^^^^^
Arguments
^^^^^^^^^^^

* ``string`` name
    name of a timer

===================
setHighResolution
===================

.. warning::

    Use this on your own risk. This may cause exceptions and other weird stuff.

Sets all timers tick rate to 10ms::

    timer.setHighResolution()

#############
Examples
#############

.. code-block:: lua

    t = timer.create("timer1", 1000, true, function()
        print("on tick")
        timer.stop("timer1")
    end)

    t.start()
