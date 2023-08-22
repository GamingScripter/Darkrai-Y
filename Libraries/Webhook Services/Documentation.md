# Darkrai Y Webhook Services Documentation

The `Darkrai Y Webhook Services` module provides functionality to send messages and embeds to Discord webhooks. It also includes various formatting options and utilities for creating and sending rich embeds.

## Table of Contents

- [Module Overview](#module-overview)
- [Importing](#importing)
- [Classes and Functions](#classes-and-functions)
- [Sending](#sending)
  - [Embed](#building-embed)
  - [Format Editor](#format-editor)
  - [Get Player Shot](#get-player-shot)
  - [Mention](#mention)
  - [Queue System](#queue-system)
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

## Sending
```lua
DYWebhook:Send({
	url = {"WEBHOOK_URL_HERE"}, -- can be more than one
	content = "Content (Normal Message)",
	embeds = {embed} -- can be more than one
})
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
