Clientside menu library
=============================================
.. highlight:: lua

.. note:: This experimental feature is in development but you can already use it

Allows you to open client-side menus from server

#############
Functions
#############

============
register
============

Registers a menu::

    cmenu.register(name, definition)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``string`` name
    unique name of a menu

* ``table`` definition
    definition of a menu

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Structure of the menu definition
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. note:: button, x, y currently didn't implement

.. code-block:: lua

    {
        title: string,
        subtitle: string,
        button: string,
        click: function,
        x: number,
        y: number,
        items: {
            {
                id: string,
                key: string,
                value: any,
                click: function
            }
        }
    }

============
unregister
============

Unregisters a menu::

    cmenu.unregister(name, definition)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``string`` name
    name of a menu

============
open
============

Registers a menu::

    cmenu.open(name, client)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``string`` name
    name of a menu

* ``Client`` client
    player for whom you want to open a menu

============
close
============

Registers a menu::

    cmenu.close(name, client)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``string`` name
    name of a menu

* ``Client`` client
    player for whom you want to close a menu

##########
Examples
##########

.. code-block:: lua

    cmenu.register("weapon", {
        title  = "Weapons",
        button = "M",
        items  = {
            {
                key = "RPG",
                click = function() print("Hello") end
            }
        }
    })

    function Server.OnPlayerFinishedDownload(player)
        cmenu.open("weapon", player)
    end
