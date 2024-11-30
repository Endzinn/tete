-- Script avançado para Blox Fruits

local ScreenGui = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local TitleLabel = Instance.new("TextLabel")
local CollectAllButton = Instance.new("TextButton")
local FarmLevelButton = Instance.new("TextButton")
local OneClickButton = Instance.new("TextButton")
local statusLabel = Instance.new("TextLabel")

-- Propriedades do ScreenGui
ScreenGui.Name = "BloxFruitsScript"
ScreenGui.Parent = game.CoreGui

-- Propriedades do MainFrame
MainFrame.Name = "MainFrame"
MainFrame.Parent = ScreenGui
MainFrame.BackgroundColor3 = Color3.new(0.1, 0.1, 0.1)
MainFrame.Position = UDim2.new(0.3, 0, 0.3, 0)
MainFrame.Size = UDim2.new(0, 400, 0, 400)

-- Propriedades do TitleLabel
TitleLabel.Name = "TitleLabel"
TitleLabel.Parent = MainFrame
TitleLabel.BackgroundColor3 = Color3.new(1, 1, 1)
TitleLabel.Size = UDim2.new(1, 0, 0.2, 0)
TitleLabel.Font = Enum.Font.SourceSans
TitleLabel.Text = "Blox Fruits Script Avançado"
TitleLabel.TextColor3 = Color3.new(0, 0, 0)
TitleLabel.TextScaled = true

-- Propriedades do CollectAllButton
CollectAllButton.Name = "CollectAllButton"
CollectAllButton.Parent = MainFrame
CollectAllButton.BackgroundColor3 = Color3.new(0.2, 0.8, 0.2)
CollectAllButton.Position = UDim2.new(0.15, 0, 0.35, 0)
CollectAllButton.Size = UDim2.new(0.3, 0, 0.2, 0)
CollectAllButton.Font = Enum.Font.SourceSans
CollectAllButton.Text = "Pegar Todos os Itens"
CollectAllButton.TextColor3 = Color3.new(0, 0, 0)
CollectAllButton.TextScaled = true

-- Propriedades do FarmLevelButton
FarmLevelButton.Name = "FarmLevelButton"
FarmLevelButton.Parent = MainFrame
FarmLevelButton.BackgroundColor3 = Color3.new(0.2, 0.8, 0.8)
FarmLevelButton.Position = UDim2.new(0.55, 0, 0.35, 0)
FarmLevelButton.Size = UDim2.new(0.3, 0, 0.2, 0)
FarmLevelButton.Font = Enum.Font.SourceSans
FarmLevelButton.Text = "Farmar Nível"
FarmLevelButton.TextColor3 = Color3.new(0, 0, 0)
FarmLevelButton.TextScaled = true

-- Propriedades do OneClickButton
OneClickButton.Name = "OneClickButton"
OneClickButton.Parent = MainFrame
OneClickButton.BackgroundColor3 = Color3.new(0.8, 0.2, 0.2)
OneClickButton.Position = UDim2.new(0.35, 0, 0.65, 0)
OneClickButton.Size = UDim2.new(0.3, 0, 0.2, 0)
OneClickButton.Font = Enum.Font.SourceSans
OneClickButton.Text = "One-Click"
OneClickButton.TextColor3 = Color3.new(0, 0, 0)
OneClickButton.TextScaled = true

-- Propriedades do statusLabel
statusLabel.Name = "statusLabel"
statusLabel.Parent = MainFrame
statusLabel.BackgroundColor3 = Color3.new(1, 1, 1)
statusLabel.Position = UDim2.new(0, 0, 0.85, 0)
statusLabel.Size = UDim2.new(1, 0, 0.15, 0)
statusLabel.Font = Enum.Font.SourceSans
statusLabel.Text = "Status: Aguardando..."
statusLabel.TextColor3 = Color3.new(0, 0, 0)
statusLabel.TextScaled = true

-- Funções para os botões
local function collectAllItems()
    statusLabel.Text = "Status: Coletando todos os itens!"
    -- Adicione aqui as funções para coletar todos os itens no jogo
end

local function farmLevel()
    statusLabel.Text = "Status: Farmando níveis!"
    -- Adicione aqui as funções para farmar níveis no jogo
end

local function oneClick()
    statusLabel.Text = "Status: One-Click ativado!"
    collectAllItems()
    farmLevel()
    -- Adicione aqui mais funcionalidades para o modo One-Click
end

CollectAllButton.MouseButton1Click:Connect(collectAllItems)
FarmLevelButton.MouseButton1Click:Connect(farmLevel)
OneClickButton.MouseButton1Click:Connect(oneClick)
