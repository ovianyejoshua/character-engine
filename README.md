# Character Engine

A complete system for creating fictional Reddit characters and generating human-sounding posts at scale.

## What it does

- Create fictional characters using a structured intake protocol (5 blocks of questions)
- Assign one of 11 personas to each character
- Generate Reddit posts that sound like that specific person wrote them on a specific day
- Track each character's growing experience log across posts
- Characters persist in the browser via localStorage

## How to deploy on Vercel

### Option 1 — Drag and drop (easiest)

1. Go to [vercel.com](https://vercel.com) and sign up or log in
2. Click "Add New Project"
3. Click "Browse" and upload the `character-engine-app` folder
4. Click Deploy
5. Done — you get a live URL immediately

### Option 2 — GitHub (recommended for sharing)

1. Create a new GitHub repository
2. Upload the contents of this folder to it
3. Go to [vercel.com](https://vercel.com) and connect your GitHub account
4. Import the repository
5. Click Deploy
6. Every time you push changes to GitHub, Vercel auto-deploys

## How users use it

1. They open the URL
2. They paste their Anthropic API key in the sidebar (stored in their browser only, never sent anywhere except Anthropic)
3. They create a character using the intake form
4. They write posts using that character
5. Characters and their experience logs are saved in their browser

## Important notes

- Each user needs their own Anthropic API key from [console.anthropic.com](https://console.anthropic.com)
- Characters are stored in the browser (localStorage) — they persist between sessions on the same browser but not across devices
- For a shared character library across users/devices, a backend database would be needed (future version)
- The app calls the Anthropic API directly from the browser — this is fine for a team tool but not ideal for a public product at scale

## The 11 personas

1. The Helpful Explainer
2. The Emotional Supporter
3. The Humble Learner
4. The Skeptical Pragmatist
5. The Angry Idealist
6. The Data-Driven Analyst
7. The Jargon Expert
8. The Long-Form Storyteller
9. The Historical Context Giver
10. The Moral Simplifier
11. The Cheerleader

## Built with

- Plain HTML, CSS, JavaScript — no frameworks, no build step
- Anthropic Claude API (claude-sonnet-4-20250514)
- Vercel for hosting
