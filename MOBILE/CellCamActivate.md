---
ns: MOBILE
---
## CELL_CAM_ACTIVATE

```c
// 0xFDE8F069C542D126 0x234C1AE9
void CELL_CAM_ACTIVATE(BOOL toggle, BOOL goFirstPerson);
```

Toggles the cellphone camera. Make sure you have a phone created with [`CREATE_MOBILE_PHONE`](#_0xA4E8E696C532FBC7) or else the camera will not work.

## Parameters
* **toggle**: 
* **goFirstPerson**: 

## Examples
```lua
local camActive = false
local selfieMode = false

RegisterCommand('cellcam', function()
    -- Remove the camera if command is called again
    if camActive then
        camActive = false
        return
    end

    camActive = true
    if IsPauseMenuActive() then SetFrontendActive(false) end -- Close pause menu if it's open

    CreateMobilePhone(3) -- Create the phone
    CellCamActivate(true, true) -- Toggle the cellphone camera ON

    -- Maintain phone while the camera is active
    while camActive do
        Wait(0)

        DisableFrontendThisFrame() -- Disable opening pause menu per frame phone is active

        if IsControlJustReleased(2, 238) or IsControlJustReleased(2, 202) then -- Listen for rightclick or esc releasing
            camActive = false -- Stop the loop and then deactivate the camera
        elseif IsControlJustReleased(2, 27) then -- Listen for scrollwheel button press to toggle selfie mode on/off
            selfieMode = not selfieMode
            CellCamActivateSelfieMode(selfieMode)
        end
    end

    selfieMode = false
    print('Camera deactivated!')
    DestroyMobilePhone()
end)```