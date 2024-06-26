---
ns: NETWORK
aliases: ["0x45F35C0EDC33B03B"]
---
## NETWORK_ADD_MAP_ENTITY_TO_SYNCHRONISED_SCENE

```c
// 0x45F35C0EDC33B03B
void NETWORK_ADD_MAP_ENTITY_TO_SYNCHRONISED_SCENE(int netScene, Hash modelHash, float x, float y, float z, cs_type(float) char* animDict, char* animName, float blendInSpeed, float blendOutSpeed, int flags);
```

Adds a map entity to a network synchronized scene. This native function is utilized only once as of game build 2944 within the casino_slots script.
Please note that it's only possible to add a single map entity to synchronized scenes.

It's advisable to initially locate the object and retrieve its actual coordinates using [`GET_CLOSEST_OBJECT_OF_TYPE`](#_0xE143FA2249364369).

```
NativeDB Introduced: v1734
```

## Parameters
* **netScene**: Net scene ID returned by [`NETWORK_CREATE_SYNCHRONISED_SCENE`](#_0x7CD6BC4C2BBDD526)
* **modelHash**: Model hash of the object the script should look for
* **x**: Object X coord
* **y**: Object Y coord
* **z**: Object Z coord
* **animDict**: Anim dictionary to play on this object (If the object was found)
* **animName**: Anim name to play on this object (If the object was found)
* **blendInSpeed**: Float representing how quickly the animation should be blended into. 2.0 is used in casino_slots
* **blendOutSpeed**: Float representing how quickly the animation should be blended out of. -1.5 is used in casino_slots
* **flags**: Animation flags. casino_slots uses 13.
