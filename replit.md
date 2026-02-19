# GoatBot V2 - Messenger Bot

## Overview
A Facebook Messenger chatbot built with Node.js, using the GoatBot V2 framework. Features a web-based dashboard for bot management.

## Project Architecture
- **Entry point**: `index.js` -> spawns `Cid.js`
- **Bot logic**: `bot/` directory (login, handlers, commands)
- **Dashboard**: `dashboard/` directory (Express web server with Eta templates)
- **FB Chat API**: `fb-chat-api/` directory (Facebook automation library - nexus-fca)
- **Commands**: `scripts/cmds/` (bot command scripts)
- **Events**: `scripts/events/` (bot event scripts)
- **Database**: SQLite (configured in config.json)
- **Config**: `config.json` (main config), `configCommands.json` (command config)

## Key Settings
- Dashboard runs on port 5000 (0.0.0.0)
- Database type: SQLite
- Template engine: Eta
- Framework: Express

## Recent Changes
- 2026-02-19: Configured for Replit environment
  - Set dashboard port to 5000, bound to 0.0.0.0
  - Removed Render keep-alive server (conflicts with dashboard port)
  - Disabled HealthServer in fb-chat-api (conflicts with dashboard port)
  - Installed system dependencies for canvas (cairo, pango, etc.)
  - Installed fb-chat-api subdirectory dependencies
  - Created .gitignore
