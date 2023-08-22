# Darkrai Y Webhook Services Documentation

The `Darkrai Y Webhook Services` module provides functionality to send messages and embeds to Discord webhooks. It also includes various formatting options and utilities for creating and sending rich embeds.

## Table of Contents

- [Module Overview](#module-overview)
- [Usage](#importing)
- [Classes and Functions](#classes-and-functions)
  - [`DYWebhookServices`](#dywebhookservices-class)
  - [Format Editor](#format-editor)
  - [Get Player Shot](#get-player-shot)
  - [Mention](#mention)
  - [Queue System](#queue-system)

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
