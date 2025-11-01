# TradeCalcs - Cable Sizing Calculator

BS 7671 compliant cable sizing calculator for UK electricians.

## Deploy to Railway

This project is ready to deploy to Railway.app

### Files Included:
- `index.html` - Main calculator page
- `assets/` - CSS and JavaScript files
- `package.json` - Node dependencies
- `railway.json` - Railway configuration

### Deploy Steps:

1. Push to GitHub or deploy directly
2. Railway will automatically detect and serve as static site
3. Configure custom domain: tradecalcs.co.uk

## Custom Domain Setup (tradecalcs.co.uk)

After deployment, in Railway:

1. Go to your project → Settings → Domains
2. Click "Custom Domain"
3. Enter: `tradecalcs.co.uk`
4. Railway will give you DNS records

Then in your domain registrar (where you bought tradecalcs.co.uk):

**Add these DNS records:**

```
Type: CNAME
Name: @ (or www)
Value: [Railway provides this - something like: xyz.railway.app]
```

Or if Railway gives A records:
```
Type: A
Name: @
Value: [IP address Railway provides]
```

DNS propagation takes 5-60 minutes.

## Project Structure

```
tradecalcs-deploy/
├── index.html (main calculator)
├── assets/
│   ├── index-CHapFL-E.css
│   └── index-qg-EXhYi.js
├── package.json
└── railway.json
```

## Features

- Real-time cable sizing calculations
- BS 7671 18th Edition compliant
- All 6 installation methods
- Voltage drop analysis
- Breaker recommendations
- Mobile-first responsive design

## Tech Stack

- React 18
- Tailwind CSS
- Vanilla JavaScript (no frameworks needed at runtime)
- Static site (no backend required)
