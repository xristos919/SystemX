-- cmd start
repeat wait() until game:IsLoaded()

game.StarterGui:SetCore("SendNotification", {
    Title = "Creator";
    Text = "Made by 7kOMGXD"; -- what the text says (ofc)
    Duration = 5;
})
wait(1)
game.StarterGui:SetCore("SendNotification", {
    Title = "SystemX";
    Text = "Starting..."; -- what the text says (ofc)
    Duration = 5;
})
wait(2)
local plr = game.Players.LocalPlayer
game.Workspace:WaitForChild("Live")
game.Workspace.Live:WaitForChild(plr.Name)
game:GetService("RunService").RenderStepped:connect(
    function()
        game:GetService("Players").LocalPlayer.PlayerGui.HUD.Bottom.SP.Visible = true
        game:GetService("Players").LocalPlayer.PlayerGui.HUD.Bottom.SP.Text = "JOIN ME DISCORD:COMING SOON...";
    end
)


_G.antigrab = false
local plr = game.Players.LocalPlayer
plr.Chatted:Connect(function(x)
    if x == "xantigrab" and _G.antigrab == false then
wait(.8)
_G.antigrab = true
local args = {
    [1] = "System: Anti-grab Activated",
    [2] = "All"
}

game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(unpack(args))
elseif x == "xantigrab" and _G.antigrab == true then
wait(.8)
_G.antigrab = false
local args = {
    [1] = "System: Anti-grab Deactivated",
    [2] = "All"
}

game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(unpack(args))
end
end)


-- cmd end
-- antigrab start
game:GetService("RunService").RenderStepped:Connect(function()
    for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
    if v.Name:find("MoveStart") and _G.antigrab == true then
        v:Destroy()
    if game.PlaceId == 536102540 then
     local args = {
        [1] = workspace.FriendlyNPCs:FindFirstChild("Hair Stylist")
        }
    game:GetService("Players").LocalPlayer.Backpack.ServerTraits.ChatStart:FireServer(unpack(args))
        wait(.3)
    local args = {
        [1] = {
                [1] = "Yes"
            }
        }
    
    game:GetService("Players").LocalPlayer.Backpack.ServerTraits.ChatAdvance:FireServer(unpack(args))
        wait(.3)
    local args = {
        [1] = "woah"
        }
    game:GetService("Players").LocalPlayer.Backpack.HairScript.RemoteEvent:FireServer(unpack(args))
    else
    game.Players.LocalPlayer.Character.Head:Destroy()
    end
    end
    end
    end)
    -- antigrab end

    -- Inventor and creator: 7kOMGXD
if not game:IsLoaded() then
    game.Loaded:Wait()
    end 
    local plr = game.Players.LocalPlayer
    plr.Chatted:Connect(function(x)
        if x == "xshield" then
       
             
    Character = game.Players.LocalPlayer
    Players = game.Players.LocalPlayer.Character
    pcall(function()
    Players.Humanoid:EquipTool(Character.Backpack["Energy Wave"])
    game.Players.LocalPlayer.Character["Energy Wave"]:Activate()
    wait()
    game.Players.LocalPlayer.Character:WaitForChild("Blast").Mesh:Destroy()
    game.Players.LocalPlayer.Character.Blast:Destroy()
    game.Players.LocalPlayer.Character["Energy Wave"]:Deactivate()
    end)
    wait(.3)
    Players.Humanoid:EquipTool(Character.Backpack["Super Death Beam"])
    
    game.Players.LocalPlayer.Character["Super Death Beam"]:Activate()
    wait(.3)
    game.Players.LocalPlayer.Character.Blast:Destroy()
    game.Players.LocalPlayer.Character["Super Death Beam"]:Deactivate()
    game.Players.LocalPlayer.PlayerGui.HUD.Bottom.SP.Visible = true
    game.Players.LocalPlayer.PlayerGui.HUD.Bottom.SP.Text = "System: Shield Activated"
    wait()
    local args = {
        [1] = "System: ki shield activated",
        [2] = "All"
    }
    
    game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(unpack(args))
        end
    end)


    _G.laser = false
    local plr = game.Players.LocalPlayer
    plr.Chatted:Connect(function(x)
        if x == "xlaser" and _G.laser == false then
    wait(.8)
    _G.laser = true
    local args = {
        [1] = "System: Godbreaker Activated",
        [2] = "All"
    }
    
    game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(unpack(args))
    elseif x == "xlaser" and _G.laser == true then
    wait(.8)
    _G.laser = false
    local args = {
        [1] = "System: Godbreaker Deactivated",
        [2] = "All"
    }
    
    game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(unpack(args))
    end
    end)
        
        local mouse = game.Players.LocalPlayer:GetMouse()
        mouse.KeyDown:connect(function(k)
        if k == "v" and _G.laser == true then
        game.Players.LocalPlayer.Character.Blast.Weld:destroy()
        wait()
        game.Players.LocalPlayer.Character.Blast.Anchored = false
            end
        end)
