.AutoFarm_Level = true
_G.FastAttack = true

 
 
 
 
 
 
 
 
local Library = 
loadstring(game:HttpGetAsync("https://raw.githubusercontent.com/NOOBHUBX/LoadingUI/main/NOOB%20HUB.Lua"))()
local Window = Library.CreateLib("VENOM X Hub", "Darkteam")
local Tab = Window:NewTab("Main")
local Section = Tab:NewSection("Auto Farm")
function checklevel()
    local Level = game:GetService("Players").LocalPlayer.Data.Level.Value
    if Level == 1 or Level <= 9 then
        MON = "Bandit [Lv. 5]"
        QUESTTITLE = "Bandit"
        QUESTPOS = CFrame.new(1060.0158691406, 16.424287796021, 1547.9769287109)
        MONPOS = CFrame.new(1148.8698730469, 16.432844161987, 1630.5396728516)
        QUESTNAME = "BanditQuest1"
        QUESTNUMBER = 1
        SPAWNPOINT = "Default"
        SPAWNPOINTPOS = CFrame.new(973.96197509766, 16.273551940918, 1413.2775878906)
    end
end
Method = CFrame.new(0,25,0)
 
spawn(function()
   while wait(3) do
       if Methodnow == 1 then
        Methodnow = 2
        Method = CFrame.new(0,25,0)
        else
        Methodnow = 1
        Method = CFrame.new(0,0,25)
       end
    end
end)
 
spawn(function()
   while wait() do
       if _G.WARP then
           game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true
        else
            game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false
        end
    end
end)
 
spawn(function()
    game:GetService("RunService").Heartbeat:Connect(function()
        if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Humanoid") and _G.AutoFarm_Level then
            setfflag("HumanoidParallelRemoveNoPhysics", "False")
            setfflag("HumanoidParallelRemoveNoPhysicsNoSimulate2", "False")
            game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
        end
    end)
end)
 
 
spawn(function()
    while wait() do
        if _G.AutoFarm_Level then
            pcall(function()
                checklevel()
    
                if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text,QUESTTITLE) then
                    local args = {
                        [1] = "AbandonQuest"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                    
                    if game:GetService("Players").LocalPlayer.Data.SpawnPoint.Value == SPAWNPOINT then
                        local args = {
                            [1] = "SetTeam",
                            [2] = "Pirates"
                        }
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                        wait(0.5)
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = QUESTPOS
                        wait(0.8)
                            local args = {
                                [1] = "StartQuest",
                                [2] = QUESTNAME,
                                [3] = QUESTNUMBER
                            }
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                        wait(0.8)
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = MONPOS
                    else
                        _G.WARP = true
                        repeat 
                            wait()
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = SPAWNPOINTPOS
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
                        until game:GetService("Players").LocalPlayer.Data.SpawnPoint.Value == SPAWNPOINT or _G.AutoFarm_Level == false
                        _G.WARP = false
                    end
                end
                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                    for i2,v2 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        if v.Name == MON and v2.Name == MON then
                            v2.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame
                            v2.HumanoidRootPart.CanCollide = false
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * Method
                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
local Library = 
loadstring(game:HttpGetAsync("https://raw.githubusercontent.com/NOOBHUBX/LoadingUI/main/NOOB%20HUB.Lua"))()
local Window = Library.CreateLib("VENOM X Hub", "Darkteam")
local Tab = Window:NewTab("Main")
local Section = Tab:NewSection("Auto Farm")
function checklevel()
    local Level = game:GetService("Players").LocalPlayer.Data.Level.Value
    if Level == 1 or Level <= 9 then
        MON = "Monkey [Lv. 14]"
        QUESTTITLE = "Monkey"
        QUESTPOS = CFrame.new (1384.8201904297, 22.852104187012, 120.3835067749)
        MONPOS = CFrame.new(1661.4359130859, 22.85209274292, -75.073577880859)
        QUESTNAME = nil
        QUESTNUMBER = nil
                        end
                    end
                end
            end)
        end
    end
end)
 
 
 
local Library = 
loadstring(game:HttpGetAsync("https://raw.githubusercontent.com/NOOBHUBX/LoadingUI/main/NOOB%20HUB.Lua"))()
local Window = Library.CreateLib("VENOM X Hub", "Darkteam")
local Tab = Window:NewTab("Main")
local Section = Tab:NewSection("FastAttack")
spawn(function()
   game:GetService("RunService").RenderStepped:Connect(function()
    pcall(function()
        if _G.FastAttack and _G.AutoFarm_Level then
            local Combat = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework)
            local Cemara = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework.CameraShaker)
            Cemara.CameraShakeInstance.CameraShakeState = {FadingIn = 3, FadingOut = 2, Sustained = 0, Inactive = 1}
            Combat.activeController.timeToNextAttack = 0
            Combat.activeController.hitboxMagnitude = 120
            Combat.activeController.increment = 3
        end
    end)
end) 
end)
 
 
spawn(function()
   game:GetService("RunService").RenderStepped:Connect(function()
    pcall(function()
        if _G.AutoFarm_Level then
            game:GetService'VirtualUser':CaptureController()
            game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
        end
    end)
end) 
end)







_G.SelectToolWeapon = "Combat"

_G.OnOff = true/false
_G.AutoFarm = true/false
TypeModeFarm = "TP" -- "Tween"
_G.AutoQuest = true/false
_G.AutoNew = true/false
_G.AutoThird = true/false
_G.Factory = true/false
_G.Superhuman = true/false
_G.FullSuperhuman = true/false
_G.DeathStep = true/false
_G.AutoFramEctoplasm = true/false
_G.Pole = true/false
_G.PoleHop = true/false
_G.SwanGlasses = true/false
_G.SwanGlassesHop = true/false
_G.DarkCode = true/false
_G.DarkCodeHop = true/false
_G.Bisentov2 = true/false
_G.Bisentov2Hop = true/false
_G.AutoElectricClaw = true/false
_G.Auto_Dark_Dagger_Hop = true/false
_G.AutoOpenSaber = true/false
_G.AutoFarmChest = true/false
_G.EliteHunter = true/false
_G.yama = true/false
_G.AutoRainbow = true/false
_G.AutoCitizen = true/false
_G.Equitp = true/false
_G.AutoDragonClownv2 = true/false
--- Setting Farn








local Library = loadstring(game:HttpGetAsync("https://raw.githubusercontent.com/NOOBHUBX/LoadingUI/main/NOOB%20HUB.Lua"))()
local Window = Library.CreateLib("VENOM X HUB", "DarkTheme")
local Tab = Window:NewTab("Players")
local Section = Tab:NewSection("Teleport")
 
--------------------
 
players = {}
 
for i,v in pairs(game:GetService("Players"):GetChildren()) do
   table.insert(players,v.Name)
end
 
Section:NewDropdown("Select Player", " ", players, function(abc)
    Select = abc
end)
 
 
Section:NewButton("Refresh", " ", function()
    table.clear(players)
for i,v in pairs(game:GetService("Players"):GetChildren()) do
   table.insert(players,v.Name)
end
end)
 
Section:NewButton("Teleport", " ", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[Select].Character.HumanoidRootPart.CFrame
    
    
    
    
    local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("VENOM X HUB", "DarkTheme")
local Tab = Window:NewTab("Players")
local Section = Tab:NewSection("Teleport")
 
--------------------
 
players = {}
 
for i,v in pairs(game:GetService("Players"):GetChildren()) do
   table.insert(players,v.Name)
end
 
Section:NewDropdown("Select Player", " ", players, function(abc)
    Select = abc
end)
 
 
Section:NewButton("Refresh", " ", function()
    table.clear(players)
for i,v in pairs(game:GetService("Players"):GetChildren()) do
   table.insert(players,v.Name)
end
end)
 
Section:NewButton("Teleport", " ", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[Select].Character.HumanoidRootPart.CFrame
end)







 
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("VENOM X HUB", "DarkTheme")
local Tab = Window:NewTab("Players")
local Section = Tab:NewSection("Teleport")
 
--------------------
 
players = {}
 
for i,v in pairs(game:GetService("Players"):GetChildren()) do
   table.insert(players,v.Name)
end
 
Section:NewDropdown("Select Player", " ", players, function(abc)
    Select = abc
end)
 
 
Section:NewButton("Refresh", " ", function()
    table.clear(players)
for i,v in pairs(game:GetService("Players"):GetChildren()) do
   table.insert(players,v.Name)
end
end)
 
Section:NewButton("Teleport", " ", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[Select].Character.HumanoidRootPart.CFrame
end)





----- ล่าฆ่าหัว Test 
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("VENOM X HUB", "DarkTheme")
local Tab = Window:NewTab("player")
local Section = Tab:NewSection("Kill player")
_G.Bounty_Farm_Hop = true
_G.Aimbot = true
_G.KillPlayer = true
_G.Select_Wapon_Bouty = ""
_G.Bounty_Lock = 25000000
_G.Bounty_Open = true
_G.WARP(0.8)
   end
end





---- Devil Fruit
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("VENOM X HUB", "DarkTheme")
local Tab = Window:NewTab("Main")
local Section = Tab:NewSection("Fruit")
_G.BringFruit = true/false
_G.TradeBone = true/false -- buy bone
_G.AutoStoreFruit = true/false
_G.BuyFruitSinper = true/false
_G.Select_Devil_Fruit = "" -- "Bomb-Bomb","Spike-Spike","Chop-Chop","Spring-Spring","Kilo-Kilo","Spin-Spin","Bird: Falcon","Smoke-Smoke","Flame-Flame","Ice-Ice","Sand-Sand","Dark-Dark","Diamond-Diamond","Light-Light","Love-Love","Rubber-Rubber","Barrier-Barrier","Magma-Magma","Door-Door","Quake-Quake","Human-Human: Buddha","String-String","Bird-Bird: Phoenix","Rumble-Rumble","Paw-Paw","Gravity-Gravity","Dough-Dough","Vemon-Vemon","Control-Control","Dragon-Dragon"
 ---- Misc
_G.AUTOHAKI = true
_G.BringMob = true

---- Raid
_G.autoraid = true
_G.AutoRaid_Hop = true
selectchip = "Flame" -- Ice Dark Light Rumble Magma
_G.KillAura = true
_G.NextIsland = true
_G.Awakener = true
_G.UnLock_Geppo = true/false
_G.UnLock_Ken_Haki = true/false

LockFragmentsValue = 1000
_G.LockFragments = true/false






--- Auto Farm

_G.SelectToolWeapon = "Combat"

_G.OnOff = true/false
_G.AutoFarm = true/false
TypeModeFarm = "TP" -- "Tween"
_G.AutoQuest = true/false
_G.AutoNew = true/false
_G.AutoThird = true/false
_G.Factory = true/false
_G.Superhuman = true/false
_G.FullSuperhuman = true/false
_G.DeathStep = true/false
_G.AutoFramEctoplasm = true/false
_G.Pole = true/false
_G.PoleHop = true/false
_G.SwanGlasses = true/false
_G.SwanGlassesHop = true/false
_G.DarkCode = true/false
_G.DarkCodeHop = true/false
_G.Bisentov2 = true/false
_G.Bisentov2Hop = true/false
_G.AutoElectricClaw = true/false
_G.Auto_Dark_Dagger_Hop = true/false
_G.AutoOpenSaber = true/false
_G.AutoFarmChest = true/false
_G.EliteHunter = true/false
_G.yama = true/false
_G.AutoRainbow = true/false
_G.AutoCitizen = true/false
_G.Equitp = true/false
_G.AutoDragonClownv2 = true/false
--- Setting Farn

_G.AutoFarmChest = true
_G.AutoFarmChestHop = true

_G.AlwaysCritical = true/false

_G.AttackNoCooldown = true/false

_G.NoDie = true/false
_G.No_Stun = true/false

-- Auto Rengoku
_G.AutoRengoku = true/false
RengokuWeapon = ""

-- Batolomio
_G.AutoBartilo = true/false
_G.AutoEvoRace = true/false
WeaponBartilo = ""

-- Shark man
_G.AutoSharkman
SharkmanWeapon = ""

--
_G.Observation = true/false

--
_G.FruitMastery = true/false
_G.GunMastery = true/false
WeaponMastery = ""

--- Buy
_G.LegebdarySword = true/false
_G.LegebdarySwordHop = true/false
_G.Enhancement = true/false
_G.EnhancementHop = true/false

---- Stats
_G.AutoStats = true/false
_G.Meleebf = true/false
_G.Defensebf = true/false
_G.Swordbf = true/false
_G.Gunbf = true/false
_G.Fruitbf = true/false
PointStats = 3 -- พ้อยที่ต้องการ
