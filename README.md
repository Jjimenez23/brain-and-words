# Brain & Words — Deployment Guide

## What is this
Brain & Words is an English fluency trainer app with:
- Academic Teach It Back sessions (3 phases)
- Social English mode (real conversation scenarios)
- Word Lock feature (forced vocabulary retention)
- Pattern Profile (tracks your recurring errors)
- XP, levels, streaks, badges
- Phrase bank + quiz

## How to deploy FREE on Netlify (10 minutes)

### Step 1 — Upload to GitHub
1. Go to github.com and create a new repository
2. Name it: brain-and-words
3. Upload all files from this folder (drag and drop)
4. Click Commit changes

### Step 2 — Connect to Netlify
1. Go to netlify.com and sign up free
2. Click "Add new site" > "Import an existing project"
3. Choose GitHub and select brain-and-words
4. Build settings: leave everything blank (no build command needed)
5. Click Deploy site

### Step 3 — Add your API key (important)
1. In Netlify, go to Site Settings > Environment Variables
2. Click Add a variable
3. Key: ANTHROPIC_API_KEY
4. Value: your Anthropic API key (get it from console.anthropic.com)
5. Click Save
6. Go to Deploys and click Trigger deploy

### Step 4 — Your app is live
Netlify gives you a URL like: https://brain-and-words-abc123.netlify.app
You can rename it to: https://brainandwords.netlify.app (if available)

## File structure
brain-and-words-app/
  netlify.toml              — tells Netlify where files are
  netlify/functions/
    claude.js               — serverless function (keeps API key safe)
  public/
    index.html              — the full app

## Cost
- Netlify free tier: 100GB bandwidth/month, 125k function calls/month
- Anthropic API: pay per use (very cheap for personal use, ~$0.01 per session)
