Code examples
=============================================
.. highlight:: lua

===============================
Spawn a vehicle with command
===============================

.. code-block:: lua

	cmd.add("veh", function(player, hash)
		local pos = API.getEntityPosition(player)

		hash = Enum.castTo(Enum.VehicleHash, hash)

		if (hash) then
			local veh = API.createVehicle(hash, pos, Vector3(), 0, 0, 0)
			API.setPlayerIntoVehicle(player, veh, 0)
		end
	end)
