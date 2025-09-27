# Sausage Calculator App Support Page

This repository hosts the support page for the Sausage Calculator mobile app.

## 🚀 Cloudflare Pages Setup Instructions

### Step 1: Login to Cloudflare
1. Go to [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. Navigate to **Pages** in the left sidebar

### Step 2: Create a New Project
1. Click **Create a project**
2. Select **Connect to Git**
3. Authorize Cloudflare to access your GitHub account
4. Select the `sausage-app-support` repository
5. Click **Begin setup**

### Step 3: Configure Build Settings
- **Project name**: `sausage-app-support` (or your preferred name)
- **Production branch**: `main`
- **Build command**: (leave empty - no build needed)
- **Build output directory**: `/`
- Click **Save and Deploy**

### Step 4: Custom Domain Setup
After deployment completes:

1. Go to **Custom domains** tab
2. Click **Set up a custom domain**
3. Enter: `warpedbbq.com`
4. Add the following DNS records in your domain registrar:
   ```
   Type: CNAME
   Name: @
   Content: sausage-app-support.pages.dev
   ```

### Step 5: Configure Routing
To make the page accessible at `/appsupport`:

1. In Cloudflare Pages settings, go to **Redirects**
2. Add a redirect rule:
   - From: `warpedbbq.com/appsupport`
   - To: `warpedbbq.com/index.html`
   - Status: `200` (rewrite)

Alternatively, if you want a cleaner URL structure:
1. Create an `appsupport` folder in the repo
2. Move `index.html` and `support.png` into it
3. Redeploy

### Step 6: Verify Deployment
Your support page should now be live at:
- Primary: `https://warpedbbq.com/appsupport`
- Backup: `https://sausage-app-support.pages.dev`

## 📁 Files
- `index.html` - Main support page with dark theme
- `support.png` - Screenshot of the Community Feedback feature
- `README.md` - This file with setup instructions

## 🔄 Updates
Any push to the `main` branch will automatically trigger a new deployment on Cloudflare Pages.

## 📧 Support
For questions about the app, use the Community Feedback feature as described on the support page.

---
© 2024 Sausage Calculator by Warped BBQ