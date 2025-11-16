# NgocTu-android
Script android by ngoc tu ff
-- 🔥 SCRIPT NGỌC TÚ ANDROID - BY NGỌC TÚ FF 🔥
if not game:IsLoaded() then game.Loaded:Wait() end

local Player = game:GetService("Players").LocalPlayer
print("✅ NGỌC TÚ SCRIPT LOADED!")

-- GUI ĐƠN GIẢN CHO ANDROID
local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "NgocTuMobile"
ScreenGui.Parent = Player.PlayerGui

local MainFrame = Instance.new("Frame")
MainFrame.Size = UDim2.new(0, 350, 0, 400)
MainFrame.Position = UDim2.new(0.5, -175, 0.5, -200)
MainFrame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
MainFrame.BorderColor3 = Color3.fromRGB(255, 215, 0)
MainFrame.BorderSizePixel = 2
MainFrame.Parent = ScreenGui

local Title = Instance.new("TextLabel")
Title.Size = UDim2.new(1, 0, 0, 50)
Title.Text = "👑 NGỌC TÚ ANDROID"
Title.TextColor3 = Color3.fromRGB(255, 215, 0)
Title.BackgroundColor3 = Color3.fromRGB(20, 20, 0)
Title.Font = Enum.Font.GothamBlack
Title.TextSize = 18
Title.Parent = MainFrame

local Credit = Instance.new("TextLabel")
Title.Size = UDim2.new(1, 0, 0, 20)
Title.Position = UDim2.new(0, 0, 0, 50)
Title.Text = "BY NGỌC TÚ FF"
Title.TextColor3 = Color3.fromRGB(255, 255, 0)
Title.BackgroundTransparency = 1
Title.Font = Enum.Font.GothamBold
Title.TextSize = 14
Title.Parent = MainFrame

local ScrollFrame = Instance.new("ScrollingFrame")
ScrollFrame.Size = UDim2.new(1, -10, 1, -80)
ScrollFrame.Position = UDim2.new(0, 5, 0, 75)
ScrollFrame.CanvasSize = UDim2.new(0, 0, 0, 500)
ScrollFrame.ScrollBarThickness = 8
ScrollFrame.Parent = MainFrame

-- TẠO NÚT ĐƠN GIẢN
local function CreateButton(text, yPos)
    local Button = Instance.new("TextButton")
    Button.Size = UDim2.new(1, -10, 0, 40)
    Button.Position = UDim2.new(0, 5, 0, yPos)
    Button.Text = text
    Button.BackgroundColor3 = Color3.fromRGB(255, 215, 0)
    Button.TextColor3 = Color3.fromRGB(0, 0, 0)
    Button.Font = Enum.Font.GothamBold
    Button.TextSize = 16
    Button.Parent = ScrollFrame
    
    return Button
end

-- AUTO FARM
CreateButton("🌾 AUTO FARM", 10).MouseButton1Click:Connect(function()
    _G.AutoFarm = not _G.AutoFarm
    print("Auto Farm:", _G.AutoFarm)
end)

-- GOD MODE
CreateButton("🛡️ GOD MODE", 60).MouseButton1Click:Connect(function()
    _G.GodMode = not _G.GodMode
    if _G.GodMode then
        Player.Character.Humanoid.Health = math.huge
    end
    print("God Mode:", _G.GodMode)
end)

-- FLY HACK
CreateButton("🚀 FLY HACK", 110).MouseButton1Click:Connect(function()
    _G.Fly = not _G.Fly
    print("Fly Hack:", _G.Fly)
end)

-- SPEED HACK
CreateButton("⚡ SPEED HACK", 160).MouseButton1Click:Connect(function()
    _G.Speed = not _G.Speed
    if _G.Speed then
        Player.Character.Humanoid.WalkSpeed = 50
    else
        Player.Character.Humanoid.WalkSpeed = 16
    end
    print("Speed Hack:", _G.Speed)
end)

-- INFINITE JUMP
CreateButton("🦘 INF JUMP", 210).MouseButton1Click:Connect(function()
    _G.InfJump = not _G.InfJump
    print("Infinite Jump:", _G.InfJump)
end)

-- CLOSE BUTTON
CreateButton("❌ ĐÓNG MENU", 350).MouseButton1Click:Connect(function()
    ScreenGui:Destroy()
end)

print("🎮 NGỌC TÚ SCRIPT READY!")
