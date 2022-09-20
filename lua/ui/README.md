# UI Libraries
This are the UI libs that I use in most of my Roblox Scripts, and are either remakes, modified versions, or generally just the same document just that hosted here for better reachability (atleast for me)
## Credits to their original authors

## notifs.lua
**My version of [Jxereas Notification UI Lib](https://v3rmillion.net/showthread.php?tid=1165214)**
```lua
local Notification = loadstring(game:HttpGet("", true))() -- insert url

Notification.new("error", "Error Heading", "Error body message.") -- Args(<string> Type, <string> Heading, <string> Body, <boolean?> AutoRemoveNotif, <number?> AutoRemoveTime, <function?> OnCloseFunction)
Notification.new("success", "Success Heading", "Success body message.") -- Args(<string> Type, <string> Heading, <string> Body, <boolean?> AutoRemoveNotif, <number?> AutoRemoveTime, <function?> OnCloseFunction)
Notification.new("info", "Information Heading", "Information body message.") -- Args(<string> Type, <string> Heading, <string> Body, <boolean?> AutoRemoveNotif, <number?> AutoRemoveTime, <function?> OnCloseFunction)
Notification.new("warning", "Warning Heading", "Warning body message.") -- Args(<string> Type, <string> Heading, <string> Body, <boolean?> AutoRemoveNotif, <number?> AutoRemoveTime, <function?> OnCloseFunction)
Notification.new("message", "Message Heading", "Message body message.") -- Args(<string> Type, <string> Heading, <string> Body, <boolean?> AutoRemoveNotif, <number?> AutoRemoveTime, <function?> OnCloseFunction)

local notif = Notification.new("success", "Success", "Success body message.")
notif:changeHeading("New Heading") -- Args(<string> NewHeading)
notif:changeBody("New Body") -- Args(<string> NewBody)
notif:deleteTimeout(3) -- Args(<number> DeleteWaitTime)
notif:delete()
```

## rdlib.lua
**Remake of [Flux UI](https://v3rmillion.net/showthread.php?tid=1101621)**
```lua
local Flux = loadstring(game:HttpGet(""))() -- insert url here

local win = Flux:Window("PREVIEW", "Baseplate", Color3.fromRGB(255, 110, 48), Enum.KeyCode.LeftControl)
local tab = win:Tab("Tab 1", "http://www.roblox.com/asset/?id=6023426915")
tab:Button("Kill all", "This function may not work sometimes and you can get banned.", function()
Flux:Notification("Killed all players successfully!", "Alright")
end)
tab:Label("This is just a label.")
tab:Line()
tab:Toggle("Auto-Farm Coins", "Automatically collects coins for you!", function(t)
print(t)
end)
tab:Slider("Walkspeed", "Makes your faster.", 0, 100,16,function(t)
print(t)
end)
tab:Dropdown("Part to aim at", {"Torso","Head","Penis"}, function(t)
print(t)
end)
tab:Colorpicker("ESP Color", Color3.fromRGB(255,1,1), function(t)
print(t)
end)
tab:Textbox("Gun Power", "This textbox changes your gun power, so you can kill everyone faster and easier.", true, function(t)
print(t)
end)
tab:Bind("Kill Bind", Enum.KeyCode.Q, function()
print("Killed a random person!")
end)
win:Tab("Tab 2", "http://www.roblox.com/asset/?id=6022668888")
```