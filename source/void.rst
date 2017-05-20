Stuff that exist in API but not in the library
==================================================

Here you can find some objects that can be found in GT-MP API but for some reason doesn't exist in LuaConnector and why they are not in.

###############
Functions
###############

------------
API.delay
------------

Reason: ??

--------------------------
API.fetchNativeFromPlayer
--------------------------

Reason: not yet because generic

------------
API.fromJson
------------

Reason: ??

-----------------
API.getWorldData
-----------------

Reason: not yet because dynamic

-----------------------
getWorldSyncedData
-----------------------

Reason: not yet because dynamic

----------------------
API.loadConfig
----------------------

Reason: ``xml`` module needed

----------------------
API.loadXml
----------------------

Reason: ``xml`` module needed

---------------------
API.random
---------------------

Reason: no need because there is already ``math.random``

-------------------
API.startThread
-------------------

Reason: threading

-------------------
API.toJson
-------------------

Reason: there is already :doc:`json </json>` library

----------------------------
API.getEntityFromHandle
----------------------------

Reason: not yet because generic
