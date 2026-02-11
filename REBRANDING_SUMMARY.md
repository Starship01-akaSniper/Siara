# Siara Bot - Rebranding Summary

## What Was Changed

The openclaw/openclaw repository has been cloned and rebranded to "Siara". Here's what was modified:

### Files Modified

1. **package.json**
   - Changed package name from `openclaw` to `siara`
   - Updated binary reference from `openclaw` to `siara`
   - Updated file references and Android package name

2. **openclaw.mjs → siara.mjs**
   - Renamed the main CLI entry point file

3. **render.yaml**
   - Changed service name from `openclaw` to `siara`
   - Updated environment variables:
     - `OPENCLAW_STATE_DIR` → `SIARA_STATE_DIR`
     - `OPENCLAW_WORKSPACE_DIR` → `SIARA_WORKSPACE_DIR`
     - `OPENCLAW_GATEWAY_TOKEN` → `SIARA_GATEWAY_TOKEN`
   - Renamed disk from `openclaw-data` to `siara-data`

4. **DEPLOYMENT.md** (NEW)
   - Comprehensive deployment guide for Render platform
   - Includes workarounds for free plan limitations
   - Step-by-step instructions with external ping services

## Deployment on Render (Free Plan)

### Key Points

⚠️ **Render's Free Plan Limitations:**
- No native cron jobs support
- Services spin down after 15 minutes of inactivity
- 750 hours/month limit

### Workaround Solution

Use external monitoring services to ping your app every 5 minutes:

**Recommended Services:**
1. **UptimeRobot** - Free, 5-minute intervals
2. **Cron-job.org** - Free HTTP cron jobs
3. **Better Uptime** - Free monitoring tier

### Quick Deployment Steps

```bash
# 1. Push to your GitHub
git remote add origin https://github.com/YOUR_USERNAME/siara.git
git push -u origin main

# 2. Deploy on Render
# - Connect GitHub repo
# - Render auto-detects render.yaml
# - Click "Apply" to deploy

# 3. Set up UptimeRobot
# - Create HTTP monitor
# - URL: https://siara.onrender.com/health
# - Interval: 5 minutes
```

### Environment Variables

| Variable | Value | Description |
|----------|-------|-------------|
| `PORT` | `8080` | HTTP port |
| `SIARA_STATE_DIR` | `/data/.siara` | State directory |
| `SIARA_WORKSPACE_DIR` | `/data/workspace` | Workspace path |
| `SIARA_GATEWAY_TOKEN` | Auto-generated | Gateway auth |
| `SETUP_PASSWORD` | Your password | Web UI access |

## For True Continuous Operation

If you need real cron jobs without external services, upgrade to **Render Starter ($7/month)**:

✅ No spin-down
✅ Native cron jobs
✅ Better performance
✅ More resources

## Files Location

All modified files are in:
```
C:\Users\rohan\.gemini\antigravity\scratch\siara\
```

## Next Steps

1. **Review the changes** in the repository
2. **Read DEPLOYMENT.md** for detailed deployment instructions
3. **Push to GitHub** (your own repository)
4. **Deploy to Render** using the blueprint
5. **Set up external ping service** (UptimeRobot recommended)
6. **Configure channels** (Telegram, Discord, etc.)
7. **Add API keys** for AI models (Anthropic/OpenAI)

## Documentation

- **Deployment Guide**: `C:\Users\rohan\.gemini\antigravity\scratch\siara\DEPLOYMENT.md`
- **Original README**: `C:\Users\rohan\.gemini\antigravity\scratch\siara\README.md`

## Credits

Original project: [OpenClaw](https://github.com/openclaw/openclaw) by Peter Steinberger and community.

This is a rebranded version for personal use.
