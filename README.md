-- carregar biblioteca
local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()

local Window = Fluent:CreateWindow({
Title = "Brasil hub" .. Fluent.Version,
TabWidth = 160, Size = UDim2.fromOffset(580, 460), Theme = "Dark"
})

local Tabs = {
Main = Window:AddTab({ Title = "Main" }),
Settings = Window:AddTab({ Title = "Settings", Icon = "settings" })
}

Tabs.Main:AddParagraph({ Title = "Teste", Content = "Teste" })

Tabs.Main:AddButton({ Title = "Button", Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/HeyGyt/infjump/main/main"))()
end })

local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()

local Window = Fluent:CreateWindow({
Title = "Exemplo Básico",
Size = UDim2.fromOffset(400, 300),
Theme = "Light"
})

local MainTab = Window:AddTab({ Title = "Principal" })

MainTab:AddButton({
Title = "Clique-me",
Callback = function()
print("Botão clicado!")
end
})

local Slider = MainTab:AddSlider("Volume", {
Title = "Ajuste o Volume",
Min = 0, Max = 100, Default = 50
})

Slider:OnChanged(function(Value)
print("Volume ajustado para:", Value)
end)

Fluent:Notify({
Title = "Bem-vindo",
Content = "Interface carregada com sucesso!"
})

