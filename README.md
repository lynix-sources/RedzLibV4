# Redz UI Library V4 

---

## 📦 Início Rápido

```lua
local redzlib = loadstring(game:HttpGet("https://raw.githubusercontent.com/lynix-sources/RedzLibV4/refs/heads/main/Source.lua"))()

-- Criar janela principal
local Window = redzlib:MakeWindow({
    Title = "REDz HUB : Example",
    SubTitle = "by : redz9999",
    LoadText = "redz Hub",
    Flags = "redz Hub | Example.lua"
})

-- Criar aba
local Tab = Window:MakeTab({ Name = "Testing", Icon = "Settings"})
```

---

## 👾 Exemplos de Componentes
### Icone de minimizar
```lua
Window:AddMinimizeButton({
  Button = {
    Image = "rbxassetid://15298567397"  -- Troque pelo ID correto da imagem do botão
  },
  UICorner = {true, CornerRadius = UDim.new(0.5, 0)},
  UIStroke = {false, {}}
})
```
### Convite de Discord 
```lua
Tab:AddDiscordInvite({
  DiscordTitle = "Title",
  DiscordIcon = "rbxassetid://15298567397",  -- Troque pelo ID correto da imagem do ícone
  DiscordLink = "Link"  -- Link do seu servidor Discord
})
```

### Seção
```lua
local Section = Tab:AddSection({"seção"})
```

### Parágrafo
```lua
local Paragraph = Tab:AddParagraph({"Tex lo", "parágrafo"})
```

### Botão
```lua
local Button = Tab:AddButton({
  Name = "Botão",
  Callback = function()
    print("Botão clicado!")
    Library:MakeNotify({
      Title = "Alerta!",
      Text = "Você clicou no botão!",
      Time = 3
    })
  end
})
```

### Toggle
```lua
local Toggle = Tab:AddToggle({
  Name = "toggle",
  Default = false,
  Callback = function(Value)
    if Value then
      print("/fling")
    else
      print("F a.")
    end
  end
})
```

### Dropdown
```lua
local Dropdown = Tab:AddDropdown({
  Name = "Selecionar Jogador",
  Options = {"Opção 1", "Opção 2", "Opção 3"},
  Default = {"Opção 1"},
  MultSelect = false,
  Callback = function(Value)
    print("Você escolheu: " .. Value)
  end
})
```

### Slider
```lua
local Slider = Tab:AddSlider({
  Name = "Slider",
  MinValue = 1,
  MaxValue = 10,
  Default = 5,
  Increase = 1,
  Callback = function(Value)
    print("Valor ajustado para: " .. Value)
  end
})
```

## Notificações

```lua
local Notify = Library:MakeNotify({
    Title = "Notification",
    Text = "This is a Notification",
    Time = 5
})
```
## 🛠️ Recursos

- ✅ UI totalmente animada com TweenService  
- ✅ Suporte a múltiplos temas  
- ✅ Sistema de salvar configurações (`SaveFolder`)  
- ✅ Notificações integradas  
- ✅ Keybind para minimizar janela  
- ✅ Use Notify:Wait() no final do seu código para a Library executar!
---

## 📌 Créditos
Criado por **redz9999 & lynix**.  
