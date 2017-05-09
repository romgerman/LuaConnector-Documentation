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
	Set ``CancelEventArgs.Cancel`` to ``true`` to cancel a command

=============
OnChatMessage
=============

Called when player have sent chat a message::

	function Server.OnChatCommand(sender, message, cancel)

---------
Arguments
---------

* ``Client`` sender
	a player that have sent a message

* ``string`` message
	message text

* ``CancelEventArgs`` cancel
	Set ``Cancel`` property to ``true`` to cancel sending chat message

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

=============
OnConnected
=============

Called when a player have been connected::

	function Server.OnPlayerConnected(player)

-------------
Arguments
-------------

* ``Client`` player
	a player that have been connected

==============
OnDisconnected
==============

Called when a player have been disconnected::

	function Server.OnPlayerDisconnected(player, reason)

-------------
Arguments
-------------

* ``Client`` player
	a player that have been disconnected

* ``string`` reason
	a reason why player have been disconnected

==============
OnUpdate
==============

Called on server tick::

	function Server.OnUpdate()
