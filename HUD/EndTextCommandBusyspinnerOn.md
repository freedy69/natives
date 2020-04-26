---
ns: HUD
aliases: ["0xBD12F8228410D9B4","_SHOW_LOADING_PROMPT","_END_TEXT_COMMAND_BUSY_STRING"]
---
## END_TEXT_COMMAND_BUSYSPINNER_ON

```c
// 0xBD12F8228410D9B4 0x903F5EE4
void END_TEXT_COMMAND_BUSYSPINNER_ON(int busySpinnerType);
```

```
Changes loading icon.
Doesn't get called every frame. Can be called once to show. To remove it, use BusyspinnerOff();

Icon types:
1, 2, 3 - Save icon (Spinning towards the right side of the screen)
4 - Rockstar cloud save icon (Save icon, but yellow)
5 - Loading icon (Spinning towards the left side of the screen)

Example:
BeginTextCommandBusyspinnerOn("STRING")
EndTextCommandBusyspinnerOn(4)

```

## Parameters
* **busySpinnerType**: 

