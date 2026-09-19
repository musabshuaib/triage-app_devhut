# Message Triage

A small app that classifies an incoming message into SALES, SUPPORT, REGISTRATION, COMPLAINT, SECURITY or OTHER, returns JSON, and routes an action.

## What is inside

    index.html      the page (open it, type a message, run the tests)
    api/triage.js   a Vercel serverless function that calls the AI model

The page tries the AI route first. If no API key is set up, it falls back to simple local keyword rules, so the site always works. Each result shows which engine answered.

## Upload to GitHub

1. Unzip this folder on your computer.
2. On github.com, click New repository, give it a name, and create it.
3. Click Add file, then Upload files.
4. Drag in index.html, README.md and the api folder (keep api/triage.js inside the api folder).
5. Click Commit changes.

## Deploy on Vercel

1. Go to vercel.com and click Add New, then Project.
2. Import your GitHub repository.
3. Leave every setting as it is and click Deploy.
4. Open the live link. It works right away with local rules.

## Turn on the real AI

1. In your Vercel project, open Settings, then Environment Variables.
2. Add a variable named ANTHROPIC_API_KEY and paste your key as the value.
3. Go to Deployments and redeploy so the variable takes effect.

The key stays on the server and is never sent to the browser. Never paste it into index.html.

Optional: add ANTHROPIC_MODEL to pick a different model.
