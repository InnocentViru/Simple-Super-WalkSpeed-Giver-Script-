# Simple-Super-WalkSpeed-Giver-Script-
A very simple script  that i created that gives super speed (Note: You need to reset to stop the speed)

local players = game:GetService("Players")
local player = players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")

local screenGui = Instance.new("ScreenGui")
screenGui.Name = "MeuScreenGui"
screenGui.Parent = playerGui

local textButton = Instance.new("TextButton")
textButton.Name = "Meubotao"

textButton.Text = "Set Super WalkSpeed"
textButton.Size = UDim2.new(0.2, 0, 0.1, 0)
textButton.Position = UDim2.new(0.5, -textButton.Size.X.Scale * screenGui.AbsoluteSize.X / 2, 0.5, -textButton.Size.Y.Scale * screenGui.AbsoluteSize.Y / 2)
textButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
textButton.TextColor3 = Color3.fromRGB(0, 0, 0)
textButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
textButton.BorderSizePixel = 2
textButton.Font = Enum.Font.SourceSansBold
textButton.Draggable = true
textButton.Active = true

textButton.Parent = screenGui

textButton.MouseButton1Click:Connect(function()
local player = game.Players.LocalPlayer
   local character = player.Character
   local humanoid = character:FindFirstChildWhichIsA("Humanoid")

   if humanoid then
       humanoid.WalkSpeed = 999
   end
   
end)

