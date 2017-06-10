Chat commands library
==========================
.. highlight:: lua

Library for chat commands

#############
Functions
#############

============
add
============

Adds a new chat command::

    cmd.add(name, callback)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``string`` name
    name of a command (ex. "cry")

* ``function`` callback
    callback function
    ``function(client, arg1, arg2, ...)`` — all arguments is in type of ``string``

=============
remove
=============

Removes a chat command::

    cmd.remove(name)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``string`` name
    name of a command

#############
Examples
#############

.. code-block:: lua

    cmd.add("msg", function(player, text)
        if text ~= nil then
            API.sendChatMessageToPlayer(player, text)
        end
    end)
