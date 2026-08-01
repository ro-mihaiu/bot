# MIHULISH Bot Site

Standalone static website for the **MIHULISH Discord bot** — the bot used on the
MIHU player-warp Discord server.

This folder is **self-contained** (plain HTML + CSS, no build step) so it can be
copied into its own GitHub repository and deployed to its own subdomain:

- `https://bot.ro-mihaiu.xyz/commands`
- `https://bot.ro-mihaiu.xyz/about`
- `https://bot.ro-mihaiu.xyz/tos`

## Pages

| File                  | Purpose                                             |
| --------------------- | --------------------------------------------------- |
| `commands/index.html` | Full command reference for every bot command        |
| `about/index.html`    | What the bot is, what the server is, what it does   |
| `tos/index.html`      | Data/privacy policy for the bot                     |
| `index.html`          | Redirect to `/commands`                             |

## Deploying to `bot.ro-mihaiu.xyz`

1. Push this folder to its own GitHub repository (e.g. `mihu-bot-site`).
2. Enable **GitHub Pages** for the repo and serve from the repo root.
3. In your DNS provider, add a `CNAME` record:
   - **Name:** `bot`
   - **Target:** `<your-username>.github.io`
4. Wait for DNS to propagate, then open `https://bot.ro-mihaiu.xyz/commands`.

The included `CNAME` file tells GitHub Pages to serve the site at
`bot.ro-mihaiu.xyz` automatically.

## Theme

The site reuses the main `ro-mihaiu.xyz` aesthetic:

- Deep black background (`#090909`) with a subtle sakura glow
- Sakura-pink accents (`#ff8ac2`)
- Glassy cards (`border-white/10`, backdrop blur)
- Inter font, rounded corners, uppercase letter-spaced section labels

All styling lives in `assets/css/style.css` — update it to re-theme the whole site.

