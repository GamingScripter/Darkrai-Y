# Darkrai Y Webhook Services Documentation

The `DYWebhookServices` module provides functionality to send messages and embeds to Discord webhooks. It also includes various formatting options and utilities for creating and sending rich embeds.

## Table of Contents

- [Module Overview](#module-overview)
- [Usage](#usage)
- [Classes and Functions](#classes-and-functions)
  - [`DYWebhookServices`](#dywebhookservices-class)
  - [Format Editor](#format-editor)
  - [Get Player Shot](#get-player-shot)
  - [Mention](#mention)
  - [Queue System](#queue-system)

## Module Overview

The `DYWebhookServices` module is designed to interact with Discord webhooks, allowing you to send messages and rich embeds to specified URLs. It provides various utilities for formatting text, mentions, and more.

## Usage

1. Import the module:
```lua
local DYWebhook = loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Darkrai-Y/main/Libraries/Webhook%20Services/Main"))()
DYWebhook.ErrorPrinting = true
