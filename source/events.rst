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

Called when a script has been loaded::

	function Script.OnStart()

=============
OnStop
=============

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
