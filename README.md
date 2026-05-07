-- [[ КОМАНДА: СОЗДАНИЕ ГЛАВНОГО ХАБА ]] --

-- 1. Очистим старые тестовые объекты, если они есть
if workspace:FindFirstChild("Meovl_Base") then workspace.Meovl_Base:Destroy() end

-- 2. Создаем контейнер для базы
local base = Instance.new("Model", workspace)
base.Name = "Meovl_Base"

-- 3. Пол (Черный зеркальный неон)
local floor = Instance.new("Part", base)
floor.Name = "Floor"
floor.Size = Vector3.new(100, 1, 100)
floor.Position = Vector3.new(0, -0.5, 0)
floor.Anchored = true
floor.Material = Enum.Material.Reflective
floor.Color = Color3.fromRGB(15, 15, 15)

-- 4. Красивая неоновая рамка
local frame = Instance.new("Part", base)
frame.Size = Vector3.new(102, 1.1, 102)
frame.Position = Vector3.new(0, -0.6, 0)
frame.Anchored = true
frame.Material = Enum.Material.Neon
frame.Color = Color3.fromRGB(255, 0, 100) -- Розовый неон в стиле Meovl

-- 5. Текст в воздухе
local partForText = Instance.new("Part", base)
partForText.Size = Vector3.new(1,1,1)
partForText.Position = Vector3.new(0, 15, 0)
partForText.Transparency = 1
partForText.Anchored = true

local bgui = Instance.new("BillboardGui", partForText)
bgui.Size = UDim2.new(0, 500, 0, 100)
bgui.AlwaysOnTop = true

local tl = Instance.new("TextLabel", bgui)
tl.Size = UDim2.new(1, 0, 1, 0)
tl.BackgroundTransparency = 1
tl.Text = "MEOVL PRINTER TYCOON"
tl.TextColor3 = Color3.fromRGB(255, 255, 255)
tl.TextStrokeTransparency = 0
tl.Font = Enum.Font.LuckiestGuy
tl.TextSize = 50

-- 6. Эффект тумана для атмосферы
game:GetService("Lighting").FogEnd = 300
game:GetService("Lighting").FogColor = Color3.fromRGB(20, 0, 20)

print("MEOVL: Локация построена! Проверь карту!")-
