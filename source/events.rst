Events
=============================================
.. highlight:: lua

#############
Script
#############

Events that gets called when something happend with script

=============
OnStart
=============

.. note::
	Very first call is happening when LuaConnector was loaded by a server (in ``API.onResourceStart`` event)

	Also called when resource gets reloaded

Called when a script has been loaded::

	function Script.OnStart()

=============
OnStop
=============

.. note::

	Latest call happends when server calls ``API.onResourceStop`` event in LuaConnector

	Also called when resource gets reloaded

Called when a ascript has been unloaded::

	function Script.OnStop()

#############
Server
#############

These events fires when something is happened on server

==============
OnUpdate
==============

Called on server tick::

	function Server.OnUpdate()

Reference `OnUpdate <https://wiki.gt-mp.net/index.php?title=OnUpdate>`_

==========================
OnPlayerBeginConnect
==========================

Called when player started initiating connection with server::

	function Server.OnPlayerBeginConnect(player, cancel)

---------
Arguments
---------

* ``Client`` player

* ``CancelEventArgs`` cancel

Reference `OnPlayerBeginConnect <https://wiki.gt-mp.net/index.php?title=OnPlayerBeginConnect>`_

===================
OnPlayerConnected
===================

Called when a player have been connected::

	function Server.OnPlayerConnected(player)

-------------
Arguments
-------------

* ``Client`` player
	a player that have been connected

Reference `OnPlayerConnected <https://wiki.gt-mp.net/index.php?title=OnPlayerConnected>`_

=====================
OnPlayerDisconnected
=====================

Called when a player have been disconnected::

	function Server.OnPlayerDisconnected(player, reason)

-------------
Arguments
-------------

* ``Client`` player
	a player that have been disconnected

* ``string`` reason
	a reason why player have been disconnected

Reference `OnPlayerDisconnected <https://wiki.gt-mp.net/index.php?title=OnPlayerDisconnected>`_

=============
OnChatCommand
=============

Called when any chat command was called::

	function Server.OnChatCommand(sender, command, cancel)

---------
Arguments
---------

* ``Client`` sender
	a player that called a command

* ``string`` command
	command that was called

* ``CancelEventArgs`` cancel
	Set ``Cancel`` property to ``true`` to cancel a command

Reference `OnChatCommand <https://wiki.gt-mp.net/index.php?title=OnChatCommand>`_

=============
OnChatMessage
=============

Called when player have sent chat a message::

	function Server.OnChatMessage(sender, message, cancel)

---------
Arguments
---------

* ``Client`` sender
	a player that have sent a message

* ``string`` message
	message text

* ``CancelEventArgs`` cancel
	Set ``Cancel`` property to ``true`` to cancel sending chat message

Reference `OnChatMessage <https://wiki.gt-mp.net/index.php?title=OnChatMessage>`_

=============
OnClientEvent
=============

Called when client event was received::

	function Server.OnClientEvent(sender, event, args)

---------
Arguments
---------

* ``Client`` sender
	a player that have sent an event

* ``string`` event
	event name

* ``table`` args
	event arguments

Reference `OnClientEventTrigger <https://wiki.gt-mp.net/index.php?title=OnClientEventTrigger>`_

===================
OnEntityDataChange
===================

Called when entity data changes::

	function Server.OnEntityDataChange(entity, key, oldVal)

---------
Arguments
---------

* ``NetHandle`` entity

* ``string`` key

* ``any`` oldVal

Reference `OnEntityDataChange <https://wiki.gt-mp.net/index.php?title=OnEntityDataChange>`_

=======================
OnEntityEnterColShape
=======================

Called when entity enters a collision shape::

	function Server.OnEntityEnterColShape(colshape, entity)

---------
Arguments
---------

* ``ColShape`` colshape

* ``NetHandle`` entity

Reference `OnEntityEnterColShape <https://wiki.gt-mp.net/index.php?title=OnEntityEnterColShape>`_

=======================
OnEntityExitColShape
=======================

Called when entity exits a collision shape::

	function Server.OnEntityExitColShape(colshape, entity)

---------
Arguments
---------

* ``ColShape`` colshape

* ``NetHandle`` entity

Reference `OnEntityExitColShape <https://wiki.gt-mp.net/index.php?title=OnEntityExitColShape>`_

==========================
OnPickupRespawn
==========================

Called when a pickup respawn::

	function Server.OnPickupRespawn(pickup)

---------
Arguments
---------

* ``NetHandle`` pickup

Reference `OnPickupRespawn <https://wiki.gt-mp.net/index.php?title=OnPickupRespawn>`_


==========================
OnPlayerArmorChange
==========================

Called when player armor changes::

	function Server.OnPlayerArmorChange(player, oldVal)

---------
Arguments
---------

* ``Client`` player

* ``number`` oldVal

Reference `OnPlayerArmorChange <https://wiki.gt-mp.net/index.php?title=OnPlayerArmorChange>`_

==========================
OnPlayerDeath
==========================

Called when player have died::

	function Server.OnPlayerDeath(player, killer, weapon)

---------
Arguments
---------

* ``Client`` pickup

* ``NetHandle`` killer

* ``number`` weapon

Reference `OnPlayerDeath <https://wiki.gt-mp.net/index.php?title=OnPlayerDeath>`_

==========================
OnPlayerDetonateStickies
==========================

Called when player detonate sticky bombs::

	function Server.OnPlayerDetonateStickies(player)

---------
Arguments
---------

* ``Client`` player

Reference `OnPlayerDetonateStickies <https://wiki.gt-mp.net/index.php?title=OnPlayerDetonateStickies>`_

==========================
OnPlayerEnterVehicle
==========================

Called when player enters a vehicle::

	function Server.OnPlayerEnterVehicle(player, vehicle)

---------
Arguments
---------

* ``Client`` player

* ``NetHandle`` vehicle

Reference `OnPlayerEnterVehicle <https://wiki.gt-mp.net/index.php?title=OnPlayerEnterVehicle>`_

==========================
OnPlayerExitVehicle
==========================

Called when player exists vehicle::

	function Server.OnPlayerExitVehicle(player, vehicle)

---------
Arguments
---------

* ``Client`` player

* ``NetHandle`` vehicle

Reference `OnPlayerExitVehicle <https://wiki.gt-mp.net/index.php?title=OnPlayerExitVehicle>`_

============================
OnPlayerFinishedDownload
============================

Called when client have finished downloading files::

	function Server.OnPlayerFinishedDownload(player)

------------
Arguments
------------

* ``Client`` player

Reference `OnPlayerFinishedDownload <https://wiki.gt-mp.net/index.php?title=OnPlayerFinishedDownload>`_

===============================
OnPlayerHealthChange
===============================

Called when player's health has changed::

	function Server.OnPlayerHealthChange(player, oldVal)

------------
Arguments
------------

* ``Client`` player

* ``number`` oldVal

Reference `OnPlayerHealthChange <https://wiki.gt-mp.net/index.php?title=OnPlayerHealthChange>`_

=============================
OnPlayerModelChange
=============================

Called when player model has changed::

	function Server.OnPlayerModelChange(player, oldVal)

-------------
Arguments
-------------

* ``Client`` player

* ``number`` oldVal

Reference `OnPlayerModelChange <https://wiki.gt-mp.net/index.php?title=OnPlayerModelChange>`_

=========================
OnPlayerPickup
=========================

Called when player have picked up a pickup::

	function Server.OnPlayerPickup(player, pickup)

------------
Arguments
------------

* ``Client`` player

* ``NetHandle`` pickup

Reference `OnPlayerPickup <https://wiki.gt-mp.net/index.php?title=OnPlayerPickup>`_

==========================
OnPlayerRespawn
==========================

Called after player have respawned::

	function Server.OnPlayerRespawn(player)

----------------
Arguments
----------------

* ``Client`` player

Reference `OnPlayerRespawn <https://wiki.gt-mp.net/index.php?title=OnPlayerRespawn>`_

==========================
OnPlayerWeaponAmmoChange
==========================

Called when player's ammo changes::

	function Server.OnPlayerWeaponAmmoChange(player, weapon, oldVal)

-------------
Arguments
-------------

* ``Client`` player

* ``WeaponHash`` weapon

* ``number`` oldValue

Reference `OnPlayerWeaponAmmoChange <https://wiki.gt-mp.net/index.php?title=OnPlayerWeaponAmmoChange>`_

==========================
OnPlayerWeaponSwitch
==========================

Called when player changes current weapon::

	function Server.OnPlayerWeaponSwitch(player, oldVal)

-----------
Arguments
-----------

* ``Client`` player

* ``WeaponHash`` oldVal

Reference `OnPlayerWeaponSwitch <https://wiki.gt-mp.net/index.php?title=OnPlayerWeaponSwitch>`_

==========================
OnVehicleDeath
==========================

Called when vehicle gets destoyed::

	function Server.OnVehicleDeath(vehicle)

------------
Arguments
------------

* ``NetHandle`` vehicle

Reference `OnVehicleDeath <https://wiki.gt-mp.net/index.php?title=OnVehicleDeath>`_

=========================
OnVehicleDoorBreak
=========================

Called when a vehicle door breaks::

	function Server.OnVehicleDoorBreak(vehicle, index)

----------
Arguments
----------

* ``NetHandle`` vehicle

* ``number`` index

Reference `OnVehicleDoorBreak <https://wiki.gt-mp.net/index.php?title=OnVehicleDoorBreak>`_

=========================
OnVehicleHealthChange
=========================

Called when vehicle's health changes::

	function Server.OnVehicleHealthChange(vehicle, oldVal)

-----------
Arguments
-----------

* ``NetHandle`` vehicle

* ``number`` oldVal

Reference `OnVehicleHealthChange <https://wiki.gt-mp.net/index.php?title=OnVehicleHealthChange>`_

========================
OnVehicleSirenToggle
========================

Called when vehicle siren toggles::

	function Server.OnVehicleSirenToggle(vehicle, oldVal)

----------
Arguments
----------

* ``NetHandle`` vehicle

* ``boolean`` oldVal

Reference `OnVehicleSirenToggle <https://wiki.gt-mp.net/index.php?title=OnVehicleSirenToggle>`_

========================
OnVehicleTrailerChange
========================

Called when vehicle trailer changes::

	function Server.OnVehicleTrailerChange(vehicle, trailer)

-----------
Arguments
-----------

* ``NetHandle`` vehicle

* ``NetHandle`` trailer

Reference `OnVehicleTrailerChange <https://wiki.gt-mp.net/index.php?title=OnVehicleTrailerChange>`_

=========================
OnVehicleTyreBurst
=========================

Called when vehicle's tyre burst::

	function Server.OnVehicleTyreBurst(vehicle, tyre)

--------------
Arguments
--------------

* ``NetHandle`` vehicle

* ``number`` tyre

Reference `OnVehicleTyreBurst <https://wiki.gt-mp.net/index.php?title=OnVehicleTrailerChange>`_

===========================
OnVehicleWindowSmash
===========================

Called when window of vehicle was smashed by player::

	function Server.OnVehicleWindowSmash(vehicle, window)

------------
Arguments
------------

* ``NetHandle`` vehicle

* ``number`` window

Reference `OnVehicleWindowSmash <https://wiki.gt-mp.net/index.php?title=OnVehicleWindowSmash>`_
