local size = 2
 
local Players = cloneref(game:GetService("Players"))
local RS = cloneref(game:GetService("RunService"))
local Client = Players.LocalPlayer
RS.RenderStepped:Connect(function ()
    for _, Player in pairs(Players:GetPlayers()) do
        if Player == Client then continue end
        local HRP = Player.Character:WaitForChild("HumanoidRootPart")
        HRP.Size = Vector3.new(size, size, size)
        HRP.CanCollide = false
        HRP.Transparency = 0.5
    end
end)
