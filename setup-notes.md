# 9Router Backup

Backup of 9Router configuration.

## Files

- `Dockerfile` - Docker image for 9Router deployment
- `package.json` - Node.js package definition
- `setup-notes.md` - Setup notes for restoring on new machine

## Original Setup

- 9Router runs on port 80 inside container
- Uses `decolua/9router:latest` image
- Deployed on Back4app (per GitHub repo description)

## Local Setup (on this machine)

- 9Router CLI installed via npm globally
- Config at: `C:\Users\hans_\AppData\Roaming\9router\`
- Tailscale integration for tunneling

## Setup on New Machine

### Option A: Docker (recommended)
```bash
docker build -t my-9router .
docker run -d -p 80:80 my-9router
```

### Option B: Local
```bash
npm install -g 9router
9router start
```

## Notes

- Backup created on 2026-07-19
- Local config (`AppData\Roaming\9router\`) NOT included (machine-specific runtime state)
- For full restore, need to also backup that directory
