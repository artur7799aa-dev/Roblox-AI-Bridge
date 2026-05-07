-- [[ MEOVL TYCOON SYSTEM: MONEY & INCOME ]] --
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(player)
    -- Создаем папку статистики
    local leaderstats = Instance.new("Folder")
    leaderstats.Name = "leaderstats"
    leaderstats.Parent = player

    -- Создаем валюту
    local money = Instance.new("IntValue")
    money.Name = "Money"
    money.Value = 0 -- Начальный баланс
    money.Parent = leaderstats

    -- Цикл дохода (Принтеры работают!)
    task.spawn(function()
        while true do
            task.wait(5) -- Каждые 5 секунд
            money.Value = money.Value + 10
            print("MEOVL: Доход начислен игроку " .. player.Name)
        end
    end)
end)

print("MEOVL: Система денег успешно загружена через GitHub!")
