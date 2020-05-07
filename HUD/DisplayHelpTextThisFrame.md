---
ns: HUD
---
## DISPLAY_HELP_TEXT_THIS_FRAME

```c
// 0x960C9FF8F616E41C 0x18E3360A
void DISPLAY_HELP_TEXT_THIS_FRAME(text entry: string, BOOL p1);
```

```
Displays help text every frame. 
The bool appears to always be false (if it even is a bool, as it's represented by a zero)
--------  
p1 doesn't seem to make a difference, regardless of the state it's in.   
Isn't displayed in the 'info' pause menu tab.
```
## Examples
```js
AddTextEntry("HELPMESSAGE", "This help message will be called every frame.");
while (true) {
	await Wait(0);
	DisplayHelpTextThisFrame("HELPMESSAGE", false);
}
```

## Parameters
* **message**: 
* **p1**: 

