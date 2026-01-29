# Clawdbot Telegram Mini App

A comprehensive interface for managing Clawdbot agents and files directly from Telegram.

## Features

- 🤖 **Agent Management**: Create, monitor, and control AI agents
- 📁 **File Browser**: Browse and access files on the host system
- 📊 **System Monitoring**: Real-time system status and metrics
- ⚡ **Quick Actions**: Fast access to common operations

## Architecture

The application consists of:
- **Frontend**: Responsive web interface using Telegram Web Apps API
- **Backend**: Express.js API server interfacing with Clawdbot
- **Integration**: Direct connection to Clawdbot tools and skills

## Deployment

This application is designed for deployment on platforms like Render, Railway, or similar PaaS providers.

### Deploy to Render

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy)

### Manual Deployment

1. Clone this repository
2. Install dependencies: `npm install`
3. Start the server: `node api/server.js`

## API Endpoints

- `GET /api/status` - System status information
- `GET /api/agents` - List active agents
- `POST /api/agents` - Create new agent
- `DELETE /api/agents/:id` - Stop an agent
- `GET /api/files?path=:path` - Browse files at path

## Integration with Telegram

To use as a Telegram Mini App:
1. Deploy this application to a public URL
2. Create a bot with [@BotFather](https://t.me/BotFather)
3. Use `/setwebapp` command to link your bot to this app

## Security

- Input validation on all endpoints
- Path traversal protection in file browsing
- Restricted file system access

## Contributing

Feel free to fork and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.