# Update-sep

## Render deployment

Use the following settings for the Node service:

- **Build command:** `npm install && npx puppeteer browsers install chrome`
- **Start command:** `npm start` (equivalent to `node bot.js`)

The application entry point is `bot.js`. The previous uploaded filename was not referenced by the Render start command, which caused `MODULE_NOT_FOUND` errors.

Configure these Render environment variables before starting the service:

- `BOT_TOKEN` — Telegram bot token. Rotate the previously exposed token before redeploying.
- `OWNER_PASS` — owner login password. Rotate the previously committed password before redeploying.
- `PORT` — supplied automatically by Render.
- `RENDER_URL` — optional public service URL for the keep-alive ping.
