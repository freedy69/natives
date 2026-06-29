---
ns: HUD
---
## IS_HELP_MESSAGE_BEING_DISPLAYED

```c
// 0x4D79439A6B55AC67 0xA65F262A
BOOL IS_HELP_MESSAGE_BEING_DISPLAYED();
```


## Return value
Unlike [`IS_HELP_MESSAGE_ON_SCREEN`](#_0xDAD37F45428801AE), which takes one frame to return true after calling [`END_TEXT_COMMAND_DISPLAY_HELP`](#_0x238FFE5C7B0498A6), this native will return true instantly.
