---
ns: VEHICLE
---
## GET_RANDOM_VEHICLE_FRONT_BUMPER_IN_SPHERE

```c
// 0xC5574E0AEB86BA68 0xDCADEB66
Vehicle GET_RANDOM_VEHICLE_FRONT_BUMPER_IN_SPHERE(float x, float y, float z, float radius, int modelHash, int Flags, int VehicleToBeIgnored);
```

```
Flags:
    VEHICLE_SEARCH_FLAG_RETURN_LAW_ENFORCER_VEHICLES					= 1,
    VEHICLE_SEARCH_FLAG_RETURN_MISSION_VEHICLES							= 2,
    VEHICLE_SEARCH_FLAG_RETURN_RANDOM_VEHICLES							= 4,
    VEHICLE_SEARCH_FLAG_RETURN_VEHICLES_CONTAINING_GROUP_MEMBERS		= 8,
    VEHICLE_SEARCH_FLAG_RETURN_VEHICLES_CONTAINING_A_PLAYER				= 16,
    VEHICLE_SEARCH_FLAG_RETURN_VEHICLES_CONTAINING_A_DEAD_OR_DYING_PED	= 32,
    VEHICLE_SEARCH_FLAG_RETURN_VEHICLES_WITH_PEDS_ENTERING_OR_EXITING	= 64,
    VEHICLE_SEARCH_FLAG_DO_NETWORK_CHECKS								= 128,
    VEHICLE_SEARCH_FLAG_CHECK_VEHICLE_OCCUPANTS_STATES					= 256,
    VEHICLE_SEARCH_FLAG_CHECK_INTERESTING_VEHICLES						= 512,
    VEHICLE_SEARCH_FLAG_RETURN_LAW_ENFORCER_VEHICLES_ONLY				= 1024,
    VEHICLE_SEARCH_FLAG_ALLOW_VEHICLE_OCCUPANTS_TO_BE_PERFORMING_A_SCRIPTED_TASK = 2048,
    VEHICLE_SEARCH_FLAG_RETURN_HELICOPTORS_ONLY							= 4096,
    VEHICLE_SEARCH_FLAG_RETURN_BOATS_ONLY								= 8192,
    VEHICLE_SEARCH_FLAG_RETURN_PLANES_ONLY								= 16384,
    VEHICLE_SEARCH_FLAG_ALLOW_LAW_ENFORCER_VEHICLES_WITH_WANTED_LEVEL	= 32768,
    VEHICLE_SEARCH_FLAG_ALLOW_VEHICLE_OCCUPANTS_TO_BE_PERFORMING_A_NON_DEFAULT_TASK = 65536,
    VEHICLE_SEARCH_FLAG_ALLOW_TRAILERS									= 131072,
    VEHICLE_SEARCH_FLAG_ALLOW_BLIMPS									= 262144,
    VEHICLE_SEARCH_FLAG_ALLOW_SUBMARINES								= 524288
```

## Parameters
* **x**: 
* **y**: 
* **z**: 
* **radius**: 
* **modelHash**: 
* **Flags**: 
* **VehicleToBeIgnored**: 

## Return value

## Examples
```lua
RegisterCommand('TestNative', function()
    local veh = GetVehiclePedIsIn(PlayerPedId(), false)
    if veh == 0 then return end
    local coords = GetEntityCoords(veh)
    local model = GetEntityModel(veh)
    local OffsetCoords = GetOffsetFromEntityInWorldCoords(veh, 0.0, 5.0, 0.0)
    local heading = GetEntityHeading(veh) - 180.0
    local newVeh = CreateVehicle(model, OffsetCoords.x, OffsetCoords.y, OffsetCoords.z, heading, true, false)
    local test = GetRandomVehicleFrontBumperInSphere(coords.x, coords.y, coords.z, 6.0, model, 2, 0)
    Wait(1000)
    DeleteEntity(test)
end, false)
```
