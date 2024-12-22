---
ns: VEHICLE
---
## CREATE_SCRIPT_VEHICLE_GENERATOR

```c
// 0x9DEF883114668116 0x25A9A261
int CREATE_SCRIPT_VEHICLE_GENERATOR(float x, float y, float z, float heading, float MaxLength, float MaxWidth, Hash modelHash, int Remap1, int Remap2, int Remap3, int Remap4, BOOL HighPriorityFlag, BOOL ChanceOfVehicleAlarm, BOOL ChanceOfLocked, BOOL PreventEntryIfNotQualified, BOOL CanBeStolen, int livery);
```

```
Creates a script vehicle generator at the given coordinates. 
Parameters:  
a/w/s - Generator position  
heading - Generator heading  
MaxLength - (always 5.0)  
MaxWidth - (always 3.0)  
modelHash - Vehicle model hash  
Remap1/Remap2/Remap3/Remap4 - (always -1)  
HighPriorityFlag - (usually TRUE, only one instance of FALSE)  
ChanceOfVehicleAlarm/ChanceOfLocked - (always FALSE)  
PreventEntryIfNotQualified - (usally FALSE, only two instances of TRUE)  
CanBeStolen - (always TRUE)  
livery - (always -1)  
Vector3 coords = GET_ENTITY_COORDS(PLAYER_PED_ID(), 0);	CREATE_SCRIPT_VEHICLE_GENERATOR(coords.x, coords.y, coords.z, 1.0f, 5.0f, 3.0f, GET_HASH_KEY("adder"), -1. -1, -1, -1, -1, true, false, false, false, true, -1);  
```

## Parameters
* **x**: 
* **y**: 
* **z**: 
* **heading**: 
* **MaxLength**: 
* **MaxWidth**: 
* **modelHash**: 
* **Remap1**: 
* **Remap2**: 
* **Remap3**: 
* **Remap4**: 
* **HighPriorityFlag**: 
* **ChanceOfVehicleAlarm**: 
* **ChanceOfLocked**: 
* **PreventEntryIfNotQualified**: 
* **CanBeStolen**: 
* **livery**: 

## Return value
