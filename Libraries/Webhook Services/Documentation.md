# Darkrai Y Webhook Services Documentation

The `Darkrai Y Webhook Services` module provides functionality to send messages and embeds to Discord webhooks. It also includes various formatting options and utilities for creating and sending rich embeds.

## Table of Contents

- [Module Overview](#module-overview)
- [Importing](#importing)
- [Classes and Functions](#classes-and-functions)
  - [Embed](#building-embed)
  - [Format Editor](#format-editor)
  - [Get Player Shot](#get-player-shot)
  - [Mention](#mention)
  - [Color Converter](#color-converter)
- [Sending](#sending)

## Module Overview

The `Darkrai Y Webhook Services` module is designed to interact with Discord webhooks, allowing you to send messages and rich embeds to specified URLs. It provides various utilities for formatting text, mentions, and more.

## Importing

1. Import the module:
```lua
local DYWebhook = loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Darkrai-Y/main/Libraries/Webhook%20Services/Main"))()
DYWebhook.ErrorPrinting = true
```

## Building Embed

1. Make A Embed Variable
```lua
local embed = DYWebhook.BuildEmbed()
```

2. Edit Its Properties To Your Liking
```lua
  embed.Info = {
  	Settings = {
  		Color = DYWebhook.ColorConverter(Color3.fromRGB(0,0,0))
  	},
  	Embed = {
  		Title = "Embed Title",
  		Description = "Embed Description",
  		Fields = {
  			{name = "Field 1", value = "Field Value", inline = false},
  			{name = "Field 2", value = "Field Value", inline = false},
  		},
  		Footer = "Footer Text",
  		Image = DYWebhook.GetPlayerShot.Avatar(4923724712, DYWebhook.Size["420x420"]),
  		FooterIcon = DYWebhook.GetPlayerShot.Avatar(4923724712, DYWebhook.Size["420x420"]),
  		Thumbnail = DYWebhook.GetPlayerShot.Avatar(4923724712, DYWebhook.Size["420x420"])
  	}
  }
```

## Format Editor

The `Darkrai Y Webhook Services` provides functions to format text for embedding.

### Italic

Formats text in *italic* style.
```lua
local formattedText = DYWebhook.FormatEditor.Italic("Italic Text")
```

### Bold

Formats text in **bold** style.
```lua
local formattedText = DYWebhook.FormatEditor.Bold("Bold Text")
```

### Bold Italic

Formats text in ***bold italic*** style.
```lua
local formattedText = DYWebhook.FormatEditor.BoldItalic("Bold Italic Text")
```

### Underline

Formats text in __underline__ style.
```lua
local formattedText = DYWebhook.FormatEditor.Underline("Underlined Text")
```

### Underline Italic

Formats text in __*underline italic*__ style.
```lua
local formattedText = DYWebhook.FormatEditor.UnderlineItalic("Underline Italic Text")
```

### Underline Bold

Formats text in __**underline bold**__ style.
```lua
local formattedText = DYWebhook.FormatEditor.UnderlineBold("Underline Bold Text")
```

### Underline Bold Italic

Formats text in __***underline bold italic***__ style.
```lua
local formattedText = DYWebhook.FormatEditor.UnderlineBoldItalic("Underline Bold Italic Text")
```

### Strikethrough

Formats text in ~~strikethrough~~ style.
```lua
local formattedText = DYWebhook.FormatEditor.Strikethrough("Strikethrough Text")
```

### Codeblock Line

Formats text as a codeblock inline.
```lua
local formattedText = DYWebhook.FormatEditor.CodeblockLine("Codeblock Line Text")
```

### Codeblock

Formats multiline text as a codeblock with optional syntax highlighting.
```lua
local code = [[
function helloWorld()
    print("Hello, world!")
end
]]
local formattedText = DYWebhook.FormatEditor.Codeblock(code, "lua")
```

### Block Quote

Formats text as a block quote.
```lua
local formattedText = DYWebhook.FormatEditor.BlockQuote("Block Quote Text")
```

### Multi-line Block Quote

Formats multiline text as a multi-line block quote.
```lua
local text = "Line 1\nLine 2\nLine 3"
local formattedText = DYWebhook.FormatEditor.MultiLineBlockQuote(text)
```

### Spoiler

Formats text as a spoiler.
```lua
local formattedText = DYWebhook.FormatEditor.Spoiler("Spoiler Text")
```

### URL Link

Formats a URL with optional link text.
```lua
local formattedLink = DYWebhook.FormatEditor.URL("https://example.com", "Link Text")
```

## Get Player Shot

The `Darkrai Y Webhook Services` class provides functions to get different types of shots of a player's avatar.

### Headshot

Gets the headshot of a player's avatar.
```lua
local userID = 123456789 -- Replace with the user's ID
local size = DYWebhook.Size["420x420"] -- Replace with the desired size
local headshotUrl = DYWebhook.GetPlayerShot.Headshot(userID, size)
```

### Bust Shot

Gets the bust shot (upper body) of a player's avatar.
```lua
local userID = 123456789 -- Replace with the user's ID
local size = DYWebhook.Size["420x420"] -- Replace with the desired size
local bustShotUrl = DYWebhook.GetPlayerShot.BustShot(userID, size)
```

### Avatar

Gets the full avatar of a player.
```lua
local userID = 123456789 -- Replace with the user's ID
local size = DYWebhook.Size["420x420"] -- Replace with the desired size
local avatarUrl = DYWebhook.GetPlayerShot.Avatar(userID, size)
```

### Available Image Sizes

A Markdown table listing the available sizes in the `DYWebhook.Size` table:

| Size      | Value       |
|-----------|-------------|
| 48x48     | "48x48"     |
| 50x50     | "50x50"     |
| 60x60     | "60x60"     |
| 75x75     | "75x75"     |
| 100x100   | "100x100"   |
| 150x150   | "150x150"   |
| 180x180   | "180x180"   |
| 353x352   | "353x352"   |
| 420x420   | "420x420"   |
| 720x720   | "720x720"   |

You can use these values to select the appropriate size when using the `GetPlayerShot` function.

### Replace `123456789` with the actual user's ID and use the appropriate size from the provided `DYWebhook.Size` table. These functions will return the URL of the respective player shot.

## Mention

The `Darkrai Y Webhook Services` class provides functions to mention users, roles, and channels.

### User Mention

Mentions a user by their ID.
```lua
local userID = "123456789" -- Replace with the user's ID
local userMention = DYWebhook.Mention.User(userID)
```

### Role Mention

Mentions a role by its ID.
```lua
local roleID = "987654321" -- Replace with the role's ID
local roleMention = DYWebhook.Mention.Role(roleID)
```

### Channel Mention

Mentions a channel by its ID.
```lua
local channelID = "456789123" -- Replace with the channel's ID
local channelMention = DYWebhook.Mention.Channel(channelID)
```

Replace `"123456789"`, `"987654321"`, and `"456789123"` with the actual user, role, and channel IDs respectively. These functions will return the formatted mention for the respective entity.

## Color Converter

The `Darkrai Y Webhook Services` function converts a Color3 value to a Discord-compatible color code.

```lua
local color = Color3.fromRGB(255, 0, 0) -- Replace with the desired RGB values
local colorCode = DYWebhook.ColorConverter(color)
```

Replace `Color3.fromRGB(255, 0, 0)` with the actual Color3 value you want to convert. The `ColorConverter` function will return a Discord-compatible color code that you can use in your embeds.

## Sending
```lua
DYWebhook:Send({
	url = {"WEBHOOK_URL_HERE"}, -- can be more than one
	content = "Content (Normal Message)",
	embeds = {embed} -- can be more than one
})
```
