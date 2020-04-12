---
ns: HUD
aliases: ["_SET_WARNING_MESSAGE_2"]
---
## SET_WARNING_MESSAGE_WITH_HEADER

```c
// 0xDC38CC1E35B6A5D7 0x2DB9EAB5
void SET_WARNING_MESSAGE_WITH_HEADER(char* titleMsg, char* entryLine1, int flags, char* promptMsg, BOOL p4, Any p5, BOOL background, Any* p7, BOOL showBg);
```

```
C# Example :  
Function.Call(Hash._SET_WARNING_MESSAGE_2, "HUD_QUIT", "HUD_CGIGNORE", 2, "HUD_CGINVITE", 0, -1, 0, 0, 1); 

JS Example: Basic warning message with an OK key
var Wait = (ms) => new Promise(res => setTimeout(res, ms));
AddTextEntry("warning_message_header", "Header");
AddTextEntry("warning_message_first_line", "First line of text");
AddTextEntry("warning_message_second_line", "Second line of text");
while (true) {
	await Wait(0);
	SetWarningMessageWithHeader("warning_message_header", // Header text, supports formatting such as ~r~colored ~w~text
		"warning_message_first_line", // First text line, also supports formatting
		2, // Instructionalkey enum (See documentation for SetWarningMessage for a list)
		"warning_message_second_line",  // Second text line, also supports formatting
		true, // Used to toggle background, true: black background, false: no background
		-1, // Unknown
		false, // Unknown
		true // Used to toggle background, true: black background, false: no background
	);
	if (IsControlJustPressed(2, 201) || IsControlJustReleased(2, 217)) {
		console.log("OK pressed");
		break;
	}
}

You can recreate this easily with scaleforms
---------------  
Fixed native name, from before nativedb restoration.  
```

```
NativeDB Added Parameter 10: Any p9
```

## Parameters
* **titleMsg**: 
* **entryLine1**: 
* **flags**: 
* **promptMsg**: 
* **p4**: 
* **p5**: 
* **background**: 
* **p7**: 
* **showBg**: 

