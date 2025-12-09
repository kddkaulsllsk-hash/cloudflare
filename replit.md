# EdgeTunnel - Cloudflare VLESS Proxy Worker

## Overview
This is a Cloudflare Workers project that runs a VLESS proxy server on Cloudflare's edge network. It provides a web-based management panel and proxy configuration generation.

## Project Structure
- `index.js` - Main worker code (readable format)
- `_worker.js` - Minified worker code (for Pages deployment)
- `wrangler.toml` - Cloudflare Wrangler configuration
- `package.json` - Node.js dependencies

## Development
The project uses Cloudflare Wrangler for local development:
```bash
npx wrangler dev --port 5000 --ip 0.0.0.0
```

## Configuration
Environment variables in `wrangler.toml`:
- `UUID` - Unique user identifier for authentication
- `PROXYIP` - Proxy IP address for fronting

## Access
Access the panel via: `/{YOUR_UUID}`
Default UUID: `d342d11e-d424-4583-b36e-524ab1f0afa4`

## Notes
- The D1 database binding is optional and not configured locally
- Some features require Cloudflare production environment
