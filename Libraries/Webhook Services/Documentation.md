# Darkrai Y Webhook Services

**Darkrai Y Webhook Services** is a collection of Lua scripts designed for Roblox developers to interact with Discord webhooks. These scripts provide functionalities to send messages, embeds, format text, handle avatars, and manage webhook queues seamlessly.

## Introduction
Darkrai Y Webhook Services offer Roblox developers a toolkit to interact with Discord webhooks effortlessly. Whether you want to send messages, format content, handle avatars, or manage webhook queues, these scripts have got you covered.

## Table of Contents
1. [WebhookConnect](#webhookconnect)
2. [Format Editor](#format-editor)
3. [Get Player Shot](#get-player-shot)
4. [Mention](#mention)
5. [Queue System](#queue-system)
6. [Usage](#usage)
7. [Contributing](#contributing)
8. [License](#license)

## WebhookConnect
The `WebhookConnect` module is the heart of the library, containing functions to send messages, manage webhooks, and handle errors.

## Format Editor
The `Format Editor` module provides functions to format text with various styles, such as bold, italic, underline, and more.

## Get Player Shot
The `Get Player Shot` module offers functions to generate URLs for different types and sizes of player avatars.

## Mention
The `Mention` module provides functions to mention users, roles, and channels in Discord.

## Queue System
The `Queue System` module manages a queue of webhook requests to prevent rate limiting and ensure reliable delivery.

## Usage
```lua
-- Example usage of creating an embed
local embed = WebhookConnect.BuildEmbed()
embed.Info.Embed.Title = "Hello, Embed!"
embed.Info.Embed.Description = "This is an example embed."

-- Send the embed
WebhookConnect:Send({
    urls = {"webhook_url_here"},
    embeds = {embed}
})
