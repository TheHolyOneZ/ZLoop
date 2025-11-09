# ZLoop
ZLoop is a sophisticated Discord bot cog that provides an advanced automated message system for scheduling and sending repeating messages. Perfect for announcements, reminders, tips, motivational quotes, server events, and more. It supports both rich embeds and plain text messages with extensive customization options.
> 💡 **Built for the Zygnal Ecosystem — to download and use this extension, you must be part of the Zygnal Ecosystem.**  
> This extension (cog) is part of the **Zygnal Ecosystem** and is only available through its supported platforms.  
> You can use it with:  
> - The **[Discord Bot Framework](https://github.com/TheHolyOneZ/discord-bot-framework)** — ideal for developers who want full control and flexibility *(includes an integrated extension marketplace)*, or  
> - The **[ZygnalBot](https://zygnalbot.de)** — a prebuilt, plug-and-play Discord bot *(also includes an integrated extension marketplace)*.  
>
> Browse and install extensions at [zygnalbot.com/extension](https://zygnalbot.com/extension).  
> For help or community discussions, join us on Discord: [discord.gg/sgZnXca5ts](https://discord.gg/sgZnXca5ts)
# ZLoop - Advanced Discord Repeat Message System

---

## Overview

ZLoop is a sophisticated Discord bot cog that provides an advanced automated message system for scheduling and sending repeating messages. Perfect for announcements, reminders, tips, motivational quotes, server events, and more. It supports both rich embeds and plain text messages with extensive customization options.

---

## Features

### Core Features

* 🗓 **Automated Scheduling** - Send messages automatically at specified intervals (minimum 60 seconds)
* 📋 **Embed Messages** - Rich embeds with custom colors, images, fields, footers, and more
* 💬 **Plain Text Messages** - Simple text messages with variable support
* 🔔 **Mentions** - Automatically ping specific roles or users with each repeat
* 📊 **Statistics Tracking** - Monitor sent messages, errors, and performance
* 🎨 **Design Suite** - Comprehensive embed customization interface
* 📁 **Template System** - Save and reuse repeat configurations
* 💾 **Auto-Backup** - Automatic backups every 6 hours (keeps last 10)
* 🔧 **Variable System** - Dynamic content with server information
* 📁 **Pagination** - Easily manage large numbers of repeats
* ⚡ **Real-time Updates** - Changes take effect immediately

### Technical Features

* Atomic file operations for data safety
* Asynchronous I/O for performance
* Comprehensive error handling and logging
* Memory-efficient design
* Support for up to 50+ repeats per server (configurable)

---


## Setup & Permissions

### Bot Permissions Required

* Send Messages
* Embed Links
* Read Message History
* View Channels
* Mention Everyone (if using role mentions)

### User Permission System

* **Administrators** - Always have full access
* **Manage Server** - Can use ZLoop if no manager roles are set
* **ZLoop Manager Roles** - Custom roles configured per server

### Initial Setup

Use `!zloop` to open the control panel and configure:

* Maximum repeats allowed
* Minimum interval between messages
* ZLoop Manager roles

---

## Commands

| Command                                  | Description                            | Permission Required |
| ---------------------------------------- | -------------------------------------- | ------------------- |
| `!zloop` or `/zloop`                     | Opens the main ZLoop control panel     | ZLoop Manager       |
| `!repeatedit <ID>` or `/repeatedit <ID>` | Quick edit a specific repeat by its ID | ZLoop Manager       |

---

## Main Control Panel

* **Manage Repeats:** View, edit, or delete existing repeats with pagination
* **Add New Repeat:** Choose Embed or Plain Text; load from templates
* **Templates:** View, load, or delete templates
* **Statistics:** View message counts, errors, and activity
* **Settings:** Configure system-wide limits and roles
* **Help:** In-app documentation and variable reference
* **Refresh:** Reload live data

---

## Creating Repeats

### Creating an Embed Repeat

1. Click `Add New Repeat → Embed Message`
2. Fill in the modal fields:

   * **Title**: Up to 256 chars
   * **Description**: Up to 4000 chars
   * **Interval**: Time in seconds
   * **Channel ID**: Target channel
   * **Color**: Hex code (e.g., `00ff00`)

### Creating a Plain Text Repeat

1. Click `Add New Repeat → Plain Text`
2. Fill in:

   * **Message Text**: Up to 2000 chars
   * **Interval**
   * **Channel ID**

---

## Managing Repeats

### Edit Repeat Menu

* 🎨 **Design Suite:** Customize embeds (title, description, footer, fields, images, color)
* ✏️ **Quick Edit:** Modify title or message text
* ⚙️ **Settings:** Adjust interval or channel
* 👁️ **Preview:** See message and test variables
* 📋 **Duplicate:** Copy repeat configuration
* 📊 **Statistics:** View individual performance
* ⏯️ **Toggle Status:** Pause/resume repeat
* 💾 **Save as Template:** Store configuration for reuse
* 🗑️ **Delete:** Permanently remove the repeat

---

## Design Suite

### Embed Components

* **Title & Description:** Supports markdown and variables
* **Footer & Author:** With optional icons and URLs
* **Images:** Thumbnail and main image
* **Fields:** Up to 25 custom name/value pairs
* **Color & Timestamp:** Optional visual customization
* **Mentions:** Add role or user IDs for pings

---

## Templates

### Saving Templates

* Edit any repeat → **Save as Template**
* Saves all settings except timing

### Loading Templates

* Create a new repeat → **Load from Template** → Select → Set interval/channel

### Managing Templates

* View, load, or delete templates
* Unlimited count supported

---

## Settings

### Server Configuration

* **System Toggle:** Enable/disable all repeats
* **Limits:**

  * Max Repeats: 1–1000 (default 50)
  * Min Interval: 15+ seconds (default 60)
* **Manager Roles:** Define ZLoop managers

---

## Variables

| Variable         | Description          | Example Output      |
| ---------------- | -------------------- | ------------------- |
| `{server_name}`  | Server name          | My Awesome Server   |
| `{server_id}`    | Server ID            | 123456789           |
| `{time}`         | Full timestamp       | 2024-01-15 14:30:45 |
| `{date}`         | Current date         | 2024-01-15          |
| `{time_short}`   | Short time           | 14:30               |
| `{channel}`      | Channel mention      | #general            |
| `{channel_name}` | Channel name         | general             |
| `{user}`         | User mention         | @User               |
| `{user_name}`    | Username             | User                |
| `{member_count}` | Total server members | 1234                |
| `{boost_count}`  | Server boost count   | 14                  |
| `{boost_level}`  | Server boost tier    | 2                   |

---

## Use Cases

* 📢 **Announcements:** Events, updates, rules
* 🎮 **Gaming:** Tournaments, recruitment, reminders
* 📚 **Education:** Daily tips, study sessions
* 💼 **Professional:** Meetings, deadlines
* 🎨 **Creative:** Challenges, showcases
* 🤝 **Support:** Motivation, check-ins

---

## Troubleshooting

### Common Issues

* **"No permission" error:** Check roles and manager configuration
* **Messages not sending:** Verify permissions, status, and channel access
* **"Channel not found":** Channel deleted or inaccessible
* **Variables not working:** Check syntax and case-sensitivity

### Best Practices

* Start with longer test intervals (300+ sec)
* Use **Preview** before enabling
* Save templates for reuse
* Monitor **Statistics** for errors
* Backup regularly
* Use descriptive titles
* Test mentions safely

---

## Data Files

| File              | Purpose                  |
| ----------------- | ------------------------ |
| `repeats.json`    | Repeat configurations    |
| `config.json`     | Server settings          |
| `statistics.json` | Performance metrics      |
| `templates.json`  | Saved templates          |
| `backups/`        | Automatic 6-hour backups |

---

## Support

* Check in-app Help menu
* Review error logs (`data/ZLoop/zloop.log`)
* Verify bot permissions
* Confirm dependencies and directory structure


**License:** Lines 1–86 at the top of the file contain the license.

**Made by TheHolyOneZ**
