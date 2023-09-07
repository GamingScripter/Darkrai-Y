# VisualLibrary Module Documentation (W.I.P)

The `VisualLibrary` module provides functionality for creating and managing visual elements in Roblox Exploits, such as Drawing and highlights. These visual elements can be used to enhance the user interface and provide information about in-game objects.

## Table of Contents

- [Module Overview](#module-overview)
- [Importing](#importing)
- [Creating Visual Elements](#creating-visual-elements)
  - [Creating a Line](#creating-a-line)
  - [Creating a Highlight](#creating-a-highlight)
- [Utility Functions](#utility-functions)
  - [Get Bounding Box](#get-bounding-box)
  - [Get Position Points](#get-position-points)
- [Module Usage](#module-usage)
  - [Creating and Tracking Visuals](#creating-and-tracking-visuals)
  - [Removing Visuals](#removing-visuals)
  - [Editing Visuals](#editing-visuals)
- [Example Usage](#example-usage)

## Module Overview

The `VisualLibrary` module is designed to create and manage visual elements in Roblox Exploits. These visual elements can include lines and highlights, which can be used to provide visual cues and information to players.

## Importing

To use the `VisualLibrary` module in your Roblox Exploit, you can import it as follows:

```lua
local VisualLibrary = loadstring(game:HttpGet()()
```

## Creating Visual Elements

### Creating a Drawing Object

To create a line visual element, you can use the `VisualLibrary:CreateVisual` function with the `Method` parameter set to "Drawing" and the `Type` parameter set to "Line." Here's an example:

```lua
local line = VisualLibrary:CreateVisual("Drawing", {
    Type = "Line",
    Color = Color3.new(1, 0, 0), -- Replace with your desired color
    Thickness = 2, -- Replace with your desired thickness
})
```

### Creating a Highlight

To create a highlight visual element, you can use the `VisualLibrary:CreateVisual` function with the `Method` parameter set to "Highlight." Here's an example:

```lua
local highlight = VisualLibrary:CreateVisual("Highlight", {
    Target = workspace.PartToHighlight, -- Replace with the target part to highlight
    Color = Color3.new(0, 1, 0), -- Replace with your desired highlight color
    Transparency = 0.5, -- Replace with your desired transparency
    StrokeColor = Color3.new(1, 1, 1), -- Replace with your desired stroke color
    OutlineTransparency = 1, -- Replace with your desired outline transparency
})
```

## Utility Functions

### Get Bounding Box

The `GetBoundingBox` function can be used to get the bounding box of an object in the script. It returns the on-screen position, size, and corners of the bounding box.
This will be helpful if the `Tracking` function looks weird.

```lua
local onScreen, size, position = VisualLibrary:GetBoundingBox(obj)
if onScreen then
    -- Use the returned values for positioning and sizing
end
```

### Get Position Points

The `getPositionPoints` function can be used to get position points around a player's or object's bounding box. It returns a table of position points, such as top, bottom, left, right, etc., in 2D screen coordinates.

```lua
local positionPoints = VisualLibrary:getPositionPoints(playerOrObject)
if positionPoints then
    -- Access the position points as positionPoints["Top"], positionPoints["Bottom"], etc.
end
```

## Module Usage

### Creating and Tracking Visuals

You can create visual elements using the `CreateVisual` function and track them by associating them with game objects or parts. Here's an example:

```lua
-- Create a line visual element
local line = VisualLibrary:CreateVisual("Drawing", {
    Type = "Line",
    Color = Color3.new(1, 0, 0),
    Thickness = 2,
})

-- Associate the line with a game object (e.g., player's character)
line:StartTracking(player.Character, "Top") -- Track the top position of the character
```

### Removing Visuals

To remove visual elements, you can call the `Remove` function on the visual element. This will stop tracking and remove the visual element from the game.

```lua
-- Remove a visual element (e.g., the line created earlier)
line:Remove()
```

### Editing Visuals

To edit visuals elements, you can edit its `Object` directly.

```lua
-- Edit a visual element (e.g., the line created earlier)
line.Object.Visible = false
```

## Example Usage

Here's an example of how you can use the `VisualLibrary` module to create and track visual elements in your Roblox Exploit. This example creates a line that tracks the top position of a player's character:

```lua
local VisualLibrary = require(game.ServerScriptService.VisualLibrary) -- Replace with the actual path

-- Create a line visual element
local line = VisualLibrary:CreateVisual("Drawing", {
    Type = "Line",
    Color = Color3.new(1, 0, 0),
    Thickness = 2,
})

-- Associate the line with a game object (e.g., player's character)
line:StartTracking(player.Character, "Top") -- Track the top position of the character
line.Object.Thickness = 1
```

This example demonstrates how to create, track, and edit visual elements in your exploits using the `VisualLibrary`.
