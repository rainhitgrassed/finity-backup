## Create Window
```lua
local Finity = loadstring(game:HttpGet("https://raw.githubusercontent.com/Auickcode/FinityLibNewLoadstring/refs/heads/main/FinityLib.lua"))()
local FinityWindow = Finity.new(true)
FinityWindow.ChangeToggleKey(Enum.KeyCode.Semicolon)
```
## Create Tab
```lua
local VisualsCategory = FinityWindow:Category("Visuals")
local AimbotCategory = FinityWindow:Category("Aimbot")
```
## Create Section
```lua
-- Visuals Sectors
local VisualsESPSettings = VisualsCategory:Sector("ESP Settings")
local VisualsPlayerESP = VisualsCategory:Sector("Player ESP")
local VisualsItemESP = VisualsCategory:Sector("Item ESP")

-- Aimbot Sectors
local AimbotColors = AimbotCategory:Sector("Aimbot Colors")
local AimbotHotkeys = AimbotCategory:Sector("Aimbot Hotkeys")
local AimbotConfigurations = AimbotCategory:Sector("Aimbot Configurations")
```

## Create Toggle
```lua
VisualsESPSettings:Cheat(
	"Checkbox", -- Type
	"ESP Enabled", -- Name
	function(State) -- Callback function
		print("Checkbox state changed:", State)
	end
)
VisualsPlayerESP:Cheat(
	"Checkbox", -- Type
	"Player ESP Enabled", -- Name
	function(State) -- Callback function
		print("Checkbox state changed:", State)
	end
)
VisualsItemESP:Cheat(
	"Checkbox", -- Type
	"Item ESP Enabled", -- Name
	function(State) -- Callback function
		print("Checkbox state changed:", State)
	end
)

AimbotConfigurations:Cheat(
	"Checkbox", -- Type
	"Aimbot Enabled", -- Name
	function(State) -- Callback function
		print("Checkbox state changed:", State)
	end
)
```
## Create Sider
```lua
VisualsESPSettings:Cheat("Slider", "Render Distance", function(Value)
	print("Silder value changed:", Value)
end, {min = 0, max = 1500, suffix = " studs"})

AimbotConfigurations:Cheat("Slider", "Aimbot FOV", function(Value)
	print("Silder value changed:", Value)
end, {min = 0, max = 120, suffix = "°"})
```
## Create Dropdow n
```lua
VisualsESPSettings:Cheat("Dropdown", "ESP Color", function(Option)
	print("Dropdown option changed:", Option)
end, {
	options = {
		"Red",
		"White",
		"Green",
		"Pink",
		"Blue"
	}
})

AimbotConfigurations:Cheat("Dropdown", "Aimbot Mode", function(Option)
	print("Dropdown option changed:", Option)
end, {
	options = {
		"FOV",
		"Distance",
		"Visibility"
	}
})
```
