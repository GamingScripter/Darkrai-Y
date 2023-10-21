
# Aura Interface Suite (AuraIS)

its very pro trust me bro

![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/c075d655-f42e-4445-870d-f6579ae0c0b0)
![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/53caccd0-2d9f-47f1-bfdd-a109549ff680)
![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/1fde4956-cdd6-41c0-94ec-ab60225673ef)


## Table of Contents

- [Importing](#importing)
- [Creating Library](#creating-library)
  - [Window](#create-window)
  - [Tab](#create-tab)
  - [Section](#create-sections)
- [Creating Elements](#creating-elements)
  - [Button](#button)
  - [Toggle](#toggle)
  - [Textbox](#textbox)
  - [Slider](#slider)
  - [Dropdown](#dropdown)
  - [Color Picker](#color-picker)
- [Other Elements](#other-elements)
  - [Text Label](#text-label)
  - [Paragraph](#paragraph)
  - [Card](#card)
- [Notification](#notification)
  - [Side Notifications](#side-notifications)
  - [Window Notifications](#window-notifications)

## Importing

### 1. Import the module:
```lua
local AuraIS = loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Darkrai-Y/main/Libraries/AuraIS/Main"))()
```

## Creating Library

### Create Window

Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/b9ec4810-8e2f-4b7a-89b6-134cc3fca0a8)


```lua
local Library = AuraIS:CreateLibrary({
    Name = "Example", -- Name
    Icon = "rbxassetid://12974454446" -- Icon
})
```

___

### Create Tab

Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/ee9c99c6-de39-4646-ac9c-367fa887c9aa)


```lua
local SecTabDemo = Library:CreateTab("Hi" --[[ title ]], "rbxassetid://12974454446" -- [[ icon ]])
```

___

### Create Sections

#### Normal Section:


Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/1d58fd6e-dcaa-4a17-bf80-b13614483522)


```lua
local SectionDemo = TabDemo:CreateSection("Section 1" --[[ section title ]], "Normal") -- Normal
```

#### Foldable Section:


Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/f273bb51-ce58-4052-88d1-5a437aea2aef)


```lua
local SecSectionDemo = TabDemo:CreateSection("Section 2" -- [[ section title ]], "Foldable") -- Foldable
```

## Creating Elements

### Button

Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/a52452ff-4eb6-4959-a336-5caaf0b4668a)


```lua
local ButtonDemo = SectionDemo:CreateButton({
    Name = "Button Example",
    Callback = function()
        print("Button 1 clicked")
    end,
})
```

---

### Toggle

#### Switch Toggle

Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/28959316-2284-42e1-92fa-ec63c39e0782)


```lua
local SwitchToggle = SectionDemo:CreateToggle("Normal", {
    Name = "Toggle Example",
    Callback = function(Value)
        print("Toggle value: " .. tostring(Value))
    end,
})
```

#### Radio Toggle

Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/d7c0f1a9-9aa5-4969-bca4-d720ed60a585)


```lua
local RadioToggle = SectionDemo:CreateToggle("Radio", {
    Name = "Toggle Example",
    Callback = function(Value)
        print("Toggle value: " .. tostring(Value))
    end,
})
```

---

### Textbox

Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/ecc9407c-138e-4e2c-921e-a9c2b4227e9a)


```lua
local TextboxDemo = SectionDemo:CreateTextbox({
	Name = "Input Example",
	PlaceholderText = "Input Placeholder",
	RemoveTextAfterFocusLost = true,
	Callback = function(Text)
		print(Text)
	end,
 })
```

---

### Slider

Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/5e074ca0-0600-4192-b926-66914c46a625)


```lua
local SliderDemo = SectionDemo:CreateSlider({
	Name = "Slider Example",
	Value = {0, 100},
	Increment = 10,
	Suffix = "Dragons",
	CurrentValue = 10,
	Flag = "Slider1",
	Callback = function(Value)
        print(Value)
	end,
 })
```

---

### Dropdown

Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/699ef030-f26f-48bd-b9ea-c07fb4839674)


```lua
local DropdownDemo = SectionDemo:CreateDropdown({
	Name = "Dropdown Example",
	Options = {"Cake", "Pie", "Milkshake", "Cupcake"},
	CurrentOption = {"Option 1"},
	MultipleOptions = false,
	Flag = "Dropdown1",
	Callback = function(v)
		print(v)
	end,
})
```

---

### Color Picker

Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/9a17431d-c3b0-49b0-89c4-aef07e6568f4)


```lua
local ColorPickerDemo = SectionDemo:CreateColorPicker({
    Name = "Color Picker",
    Callback = function(newColor)
        print(newColor)
    end,
})
```

---

## Other Elements

### Text Label

Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/6a5e977a-2f48-4e40-be1a-c195ed8fa400)


```lua
local LabelDemo = SectionDemo:CreateLabel({
	Description = "This is a sample description"
})
```

---

### Paragraph

Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/6d0e58c8-88d3-4c17-9131-59ccfd378e71)


```lua
local ParagraphDemo = SectionDemo:CreateParagraph({
	Title = "My Paragraph",
	Description = "This is a sample paragraph."
})
```

---

### Card

Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/b6601685-a168-4c17-a2a6-6ddbe3db856a)


```lua
local CardDemo = SectionDemo:CreateCard({
	Title = "My Card",
	Description = "This is a sample card.",
	SecondaryTitle = "Card State",
	Image = "rbxassetid://14167800463",
	Buttons = {
		Button1 = {
			Name = "Button 1",
			Callback = function()
				print("Button 1 clicked")
			end
		},
		Button2 = {
			Name = "Button 2",
			Callback = function()
				print("Button 2 clicked")
			end
		}
	}
})
```

---

## Notification

### Side Notifications

Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/a7c6312a-74e0-4cc1-8c9c-fc4632cfebea)


```lua
AuraIS:Notify("Normal" , { -- Notify Demo (Normal)
			Title = "Notification Title",
			Content = "Notification Content",
			Duration = 5,
			Image = "rbxassetid://4483362458",
			Actions = {
			   Ignore = {
				  Name = "Okay!",
				  Callback = function()
				  print("The user tapped Okay!")
			   end
			},
		 },
		 })

		 AuraIS:Notify("Warning" , { -- Notify Demo (Warning)
			Title = "Notification Title",
			Content = "Notification Content",
			Duration = 5,
			Image = "rbxassetid://4483362458",
			Actions = {
			   Ignore = {
				  Name = "Okay!",
				  Callback = function()
				  print("The user tapped Okay!")
			   end
			},
		 },
		 })

		 AuraIS:Notify("Error" , { -- Notify Demo (Error)
			Title = "Notification Title",
			Content = "Notification Content",
			Duration = 5,
			Image = "rbxassetid://4483362458",
			Actions = {
			   Ignore = {
				  Name = "Okay!",
				  Callback = function()
				  print("The user tapped Okay!")
			   end
			},
		 },
		 })
```

---

### Window Notifications

Example:


![image](https://github.com/GamingScripter/Darkrai-Y/assets/102379753/ca564ed2-149f-4fef-ae04-fcb6c7de331c)


```lua
Library:Notify({ -- Notify Demo (Inside Tab)
			Title = "Notification Title",
			Content = "Notification Content",
			Duration = 5,
			Image = "rbxassetid://4483362458",
			Actions = {
			   Ignore = {
				  Name = "Okay!",
				  Callback = function()
				  print("The user tapped Okay!")
			   end
			},
		 },
		 })
```
