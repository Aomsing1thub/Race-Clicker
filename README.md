if _G.NameHEE == nil then
_G.NameHEE = "KUY"
end

if game:GetService("CoreGui"):FindFirstChild(_G.NameHEE) then
else

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("🏆 Race Clicker", "Synapse")
local Tab = Window:NewTab("Main")
local Section = Tab:NewSection("Auto Farm")

for i,v in pairs(game:GetService("CoreGui"):GetDescendants()) do -- GetDescendants
    if v.Name == "MainCorner" then
        _G.NameHEE = v.Parent.Parent.Name
    end
end

function Touch(T1,T2)
firetouchinterest(T1,T2,0)
firetouchinterest(T1,T2,1)
end

Section:NewToggle("Auto Farm", "ToggleInfo", function(state)
a3 = state
if state then
else
wait(.3)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1.2490309476852417, 3.0075321197509766, -1.1224076747894287)
end
end)
    
local Section = Tab:NewSection("Auto Click")

Section:NewToggle("Auto Click", "ToggleInfo", function(state)
a1 = state
end)

spawn(function()
while wait() do
if a1 then
pcall(function()
game:GetService'VirtualUser':CaptureController()
game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
end)
end
end
end)

Select = "Normal"

spawn(function()
while wait() do
if a3 then
pcall(function()
    if game:GetService("Workspace").LoadedWorld.WorldMain.Door.SignTimer.Transparency == 1 then
        for i,v in pairs (game:GetService("Workspace").LoadedWorld.Track:GetChildren()) do
            if a3 then
                if game:GetService("Workspace").LoadedWorld.WorldMain.Door.SignTimer.Transparency == 1 then
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Sign.CFrame
                    wait(.3)
                end
            end
        end
    else
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1.2490309476852417, 3.0075321197509766, -1.1224076747894287)
    end
end)
end
end
end)

spawn(function()
while wait() do
pcall(function()
    if a3 then
        if not game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("GGEZ") then
            local Noclip = Instance.new("BodyVelocity")
            Noclip.Name = "GGEZ"
            Noclip.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
            Noclip.MaxForce = Vector3.new(100000,100000,100000)
            Noclip.Velocity = Vector3.new(0,0,0)
        end
    else
        if game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("GGEZ") then
            game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("GGEZ"):Destroy()
        end
    end
end)
end
end)

end
