-- this script was made by yua 
local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()
 
local Window = Rayfield:CreateWindow({
   Name = "+1 speed monkey escape",
   LoadingTitle = "im back",
   LoadingSubtitle = "by yuaaaa",
   ConfigurationSaving = {
      Enabled = false,
   },
   KeySystem = false,
})
 
local MainTab = Window:CreateTab("main", 4483362458)
local WorldTab = Window:CreateTab("world autofarms", 4483362458)
local OtherTab = Window:CreateTab("other", 4483362458)
 
local AutoRebirthEnabled = false
local AutoFarmTrophiesEnabled = false
local AutoBuyCharmEnabled = false
local NoTreadmillEnabled = false
local SunkenShardsEnabled = false
local World2Enabled = false
local World3Enabled = false
local World4Enabled = false
local World5Enabled = false
local FlyEnabled = false
local FlySpeed = 50
local NoclipEnabled = false
 
MainTab:CreateToggle({
   Name = "auto rebirth",
   CurrentValue = false,
   Flag = "AutoRebirthToggle",
   Callback = function(Value)
      AutoRebirthEnabled = Value
      task.spawn(function()
         while AutoRebirthEnabled do
            pcall(function()
               game:GetService("ReplicatedStorage").Remotes.Rebirth:FireServer()
            end)
            task.wait(1)
         end
      end)
   end,
})
 
MainTab:CreateToggle({
   Name = "auto buy charm",
   CurrentValue = false,
   Flag = "AutoBuyCharmToggle",
   Callback = function(Value)
      AutoBuyCharmEnabled = Value
      task.spawn(function()
         while AutoBuyCharmEnabled do
            pcall(function()
               local Event = game:GetService("ReplicatedStorage").Remotes.BuyCharm
               Event:FireServer(1)
               Event:FireServer(2)
               Event:FireServer(3)
            end)
            task.wait(0.5)
         end
      end)
   end,
})
 
MainTab:CreateToggle({
   Name = "faster 1x speed (dont move while ts on)",
   CurrentValue = false,
   Flag = "NoTreadmillToggle",
   Callback = function(Value)
      NoTreadmillEnabled = Value
      task.spawn(function()
         local direction = 1
         while NoTreadmillEnabled do
            pcall(function()
               local character = game:GetService("Players").LocalPlayer.Character
               if character and character:FindFirstChild("Humanoid") and character:FindFirstChild("HumanoidRootPart") then
                  local moveDirection = character.HumanoidRootPart.CFrame.RightVector * direction
                  character.Humanoid:Move(moveDirection, true)
                  direction = -direction
               end
            end)
            task.wait(0.05)
         end
      end)
   end,
})
 
WorldTab:CreateToggle({
   Name = "autofarm world 1",
   CurrentValue = false,
   Flag = "AutoFarmTrophiesToggle",
   Callback = function(Value)
      AutoFarmTrophiesEnabled = Value
      task.spawn(function()
         while AutoFarmTrophiesEnabled do
            pcall(function()
               local character = game:GetService("Players").LocalPlayer.Character
               if character and character:FindFirstChild("HumanoidRootPart") then
                  character.HumanoidRootPart.CFrame = CFrame.new(-9459, 392, -257)
               end
            end)
            task.wait(0.5)
         end
      end)
   end,
})
 
WorldTab:CreateToggle({
   Name = "autofarm world 2",
   CurrentValue = false,
   Flag = "World2Toggle",
   Callback = function(Value)
      World2Enabled = Value
      task.spawn(function()
         while World2Enabled do
            pcall(function()
               local character = game:GetService("Players").LocalPlayer.Character
               if character and character:FindFirstChild("HumanoidRootPart") then
                  character.HumanoidRootPart.CFrame = CFrame.new(-3603, 158, -9381)
               end
            end)
            task.wait(0.5)
         end
      end)
   end,
})
 
WorldTab:CreateToggle({
   Name = "autofarm world 3",
   CurrentValue = false,
   Flag = "World3Toggle",
   Callback = function(Value)
      World3Enabled = Value
      task.spawn(function()
         while World3Enabled do
            pcall(function()
               local character = game:GetService("Players").LocalPlayer.Character
               if character and character:FindFirstChild("HumanoidRootPart") then
                  character.HumanoidRootPart.CFrame = CFrame.new(-8079, 284, 2740)
               end
            end)
            task.wait(0.5)
         end
      end)
   end,
})
 
WorldTab:CreateToggle({
   Name = "autofarm world 4",
   CurrentValue = false,
   Flag = "World4Toggle",
   Callback = function(Value)
      World4Enabled = Value
      task.spawn(function()
         while World4Enabled do
            pcall(function()
               local character = game:GetService("Players").LocalPlayer.Character
               if character and character:FindFirstChild("HumanoidRootPart") then
                  character.HumanoidRootPart.CFrame = CFrame.new(-7761, 22, 5740)
               end
            end)
            task.wait(0.5)
         end
      end)
   end,
})
 
WorldTab:CreateToggle({
   Name = "autofarm world 5",
   CurrentValue = false,
   Flag = "World5Toggle",
   Callback = function(Value)
      World5Enabled = Value
      task.spawn(function()
         while World5Enabled do
            pcall(function()
               local character = game:GetService("Players").LocalPlayer.Character
               if character and character:FindFirstChild("HumanoidRootPart") then
                  character.HumanoidRootPart.CFrame = CFrame.new(-1332, 26, 7562)
               end
            end)
            task.wait(0.5)
         end
      end)
   end,
})
 
OtherTab:CreateToggle({
   Name = "auto sunkenshards",
   CurrentValue = false,
   Flag = "SunkenShardsToggle",
   Callback = function(Value)
      SunkenShardsEnabled = Value
      task.spawn(function()
         while SunkenShardsEnabled do
            pcall(function()
               local shardsFolder = workspace:FindFirstChild("SunkenShards")
               if shardsFolder then
                  for _, shard in ipairs(shardsFolder:GetChildren()) do
                     if not SunkenShardsEnabled then break end
                     local targetPart = shard
                     if shard:IsA("Model") then
                        targetPart = shard.PrimaryPart or shard:FindFirstChildWhichIsA("BasePart")
                     end
                     if targetPart and targetPart:IsA("BasePart") then
                        local character = game:GetService("Players").LocalPlayer.Character
                        if character and character:FindFirstChild("HumanoidRootPart") then
                           character.HumanoidRootPart.CFrame = targetPart.CFrame
                           task.wait(0.3)
                        end
                     end
                  end
               end
            end)
            task.wait(0.5)
         end
      end)
   end,
})
 
OtherTab:CreateToggle({
   Name = "fly",
   CurrentValue = false,
   Flag = "FlyToggle",
   Callback = function(Value)
      FlyEnabled = Value
      task.spawn(function()
         local player = game:GetService("Players").LocalPlayer
         local camera = workspace.CurrentCamera
         local uis = game:GetService("UserInputService")
         local bv, bg
 
         while FlyEnabled do
            pcall(function()
               local character = player.Character
               if character and character:FindFirstChild("HumanoidRootPart") and character:FindFirstChild("Humanoid") then
                  local hrp = character.HumanoidRootPart
                  local humanoid = character.Humanoid
 
                  if not bv then
                     bv = Instance.new("BodyVelocity")
                     bv.MaxForce = Vector3.new(math.huge, math.huge, math.huge)
                     bv.Parent = hrp
                  end
                  if not bg then
                     bg = Instance.new("BodyGyro")
                     bg.MaxTorque = Vector3.new(math.huge, math.huge, math.huge)
                     bg.Parent = hrp
                  end
 
                  humanoid.PlatformStand = true
                  bg.CFrame = camera.CFrame
 
                  local moveDirection = Vector3.new()
                  if uis:IsKeyDown(Enum.KeyCode.W) then moveDirection = moveDirection + camera.CFrame.LookVector end
                  if uis:IsKeyDown(Enum.KeyCode.S) then moveDirection = moveDirection - camera.CFrame.LookVector end
                  if uis:IsKeyDown(Enum.KeyCode.A) then moveDirection = moveDirection - camera.CFrame.RightVector end
                  if uis:IsKeyDown(Enum.KeyCode.D) then moveDirection = moveDirection + camera.CFrame.RightVector end
 
                  bv.Velocity = moveDirection * FlySpeed
               end
            end)
            task.wait()
         end
 
         local character = player.Character
         if character then
            if character:FindFirstChild("HumanoidRootPart") then
               if character.HumanoidRootPart:FindFirstChild("BodyVelocity") then character.HumanoidRootPart.BodyVelocity:Destroy() end
               if character.HumanoidRootPart:FindFirstChild("BodyGyro") then character.HumanoidRootPart.BodyGyro:Destroy() end
            end
            if character:FindFirstChild("Humanoid") then
               character.Humanoid.PlatformStand = false
            end
         end
      end)
   end,
})
 
OtherTab:CreateSlider({
   Name = "fly speed",
   Range = {10, 300},
   Increment = 5,
   CurrentValue = 50,
   Flag = "FlySpeedSlider",
   Callback = function(Value)
      FlySpeed = Value
   end,
})
 
OtherTab:CreateToggle({
   Name = "noclip",
   CurrentValue = false,
   Flag = "NoclipToggle",
   Callback = function(Value)
      NoclipEnabled = Value
      game:GetService("RunService").Stepped:Connect(function()
         if NoclipEnabled then
            pcall(function()
               local character = game:GetService("Players").LocalPlayer.Character
               if character then
                  for _, part in ipairs(character:GetDescendants()) do
                     if part:IsA("BasePart") then
                        part.CanCollide = false
                     end
                  end
               end
            end)
         end
      end)
   end,
})
 
print("made by yua, we back :)))")
