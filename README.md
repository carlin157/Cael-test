local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Consistt/Ui/main/UnLeaked"))()


library.rank = "developer"
local Wm = library:Watermark("xsx example | v" .. library.version ..  " | " .. library:GetUsername() .. " | rank: " .. library.rank)
local FpsWm = Wm:AddWatermark("fps: " .. library.fps)
coroutine.wrap(function()
    while wait(.75) do
        FpsWm:Text("fps: " .. library.fps)
    end
end)()


local Notif = library:InitNotifications()

for i = 20,0,-1 do 
    task.wait(0.05)
    local LoadingXSX = Notif:Notify("Carregando Cael Hub Seja paciente.", 3, "information") -- notification, alert, error, success, information
end 

library.title = "Vigil"

library:Introduction()
wait(1)
local Init = library:Init()

local Tab1 = Init:NewTab("Cael tab")

local Section1 = Tab1:NewSection("Escritur Components")


local Label1 = Tab1:NewLabel("Example label", "left")--"left", "center", "right"

local Toggle1 = Tab1:NewToggle("Sla toggle", false, function(value)
    local vers = value and "on" or "off"
    print("one " .. vers)
end):AddKeybind(Enum.KeyCode.RightControl)

local Toggle2 = Tab1:NewToggle("Toggle", false, function(value)
    local vers = value and "on" or "off"
    print("two " .. vers)
end)

local Textbox1 = Tab1:NewTextbox("Text box 1 [auto scales // small]", "", "1", "all", "small", true, false, function(val)
    print(val)
end)

local Textbox2 = Tab1:NewTextbox("Text box 2 [medium]", "", "2", "all", "medium", true, false, function(val)
    print(val)
end)

local Textbox3 = Tab1:NewTextbox("Text box 3 [large]", "", "3", "all", "large", true, false, function(val)
    print(val)
end)

local Selector1 = Tab1:NewSelector("Selector 1", "bungie", {"fg", "fge", "fg", "fg"}, function(d)
    print(d)
end):AddOption("fge")

local Slider1 = Tab1:NewSlider("Slider 1", "", true, "/", {min = 1, max = 100, default = 20}, function(value)
    print(value)
end)


Tabs.Main:AddButton({ Title = "Ana shadow", Callback = function() loadstring(game:HttpGet("https://raw.githubusercontent.com/xscripts7/XScripts/refs/heads/XScript/ShadowHub", true))() end })
Tabs.Main:AddButton({ Title = "Ana dopamina", Callback = function() loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Dopamina-Hub-17894"))() end })
Tabs.Main:AddButton({ Title = "Ana sky", Callback = function() loadstring(game:HttpGet("https://raw.githubusercontent.com/yofriendfromschool1/Sky-Hub/main/SkyHub.txt"))()end })
Tabs.Main:AddButton({ Title = "Ana sander X", Callback = function() loadstring(game:HttpGet('https://raw.githubusercontent.com/kigredns/SanderXV4.2.2/refs/heads/main/New.lua'))() end })
Tabs.Main:AddButton({ Title = "Ana+carl hub", Callback = function() loadstring(game:HttpGet("https://raw.githubusercontent.com/carlosdaniel987/Carlos/refs/heads/main/README.md"))() end })

local FinishedLoading = Notif:Notify("Loaded xsx example", 4, "success")
