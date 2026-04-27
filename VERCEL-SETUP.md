# Vercel Setup — Step-by-Step

Read this when you're ready to sign up for Vercel. Whole thing takes ~10 minutes. Cost: $0 (Hobby tier is free and sufficient for this site).

---

## Step 1 — Create a GitHub account (skip if you have one)

Vercel deploys from GitHub, so you need a GitHub account first.

1. Go to **https://github.com/signup**
2. Sign up with your email (use `brit@maxmomentum.pro` so it's the same across tools)
3. Pick the **Free** plan
4. Verify your email

That's it. You don't need to create a repository manually — I'll do that when we push the site code.

---

## Step 2 — Sign up for Vercel

1. Go to **https://vercel.com/signup**
2. Click **Continue with GitHub** (this links the two accounts)
3. Authorize Vercel to access your GitHub (it needs this to deploy)
4. When it asks for a team name, you can use `momentum` or `brit`
5. Pick the **Hobby (Free)** plan — it includes:
   - Unlimited personal projects
   - Custom domains with free SSL
   - 100 GB bandwidth/month (we'll use <1 GB)
   - Automatic deploys from GitHub

That's the whole signup. No credit card needed.

---

## Step 3 — Tell me when you're done

Once your Vercel account is live, send me:

1. Your **GitHub username** (so I can configure the repo push)
2. Your **Vercel team/username** (visible at the top-left of the Vercel dashboard)

Then I'll:
- Scaffold the production Next.js site in this folder
- Push it to a new GitHub repo (`momentum-site`)
- Connect Vercel to the repo (you'll click "Import" and approve)
- Verify it deploys to a `.vercel.app` preview URL

---

## Step 4 — DNS / Domain setup (we'll do this at the very end)

Your domain `maxmomentum.pro` is currently pointing at Squarespace. When the new site is ready on a Vercel preview URL and you've approved it, we'll swap DNS so `maxmomentum.pro` points at Vercel instead.

This is the **only step with any real risk** — during the DNS swap (usually a few minutes to a few hours of propagation), some visitors might see the old Squarespace, some the new Vercel site. We'll time this for a low-traffic window (evening/weekend) and I'll give you exact instructions when we get there.

The steps will be:
1. Log into your domain registrar (wherever you bought `maxmomentum.pro` — Squarespace, GoDaddy, Namecheap, Google Domains, etc.)
2. Find DNS settings
3. Update two records (Vercel gives us the exact values to paste)
4. Wait for propagation
5. Verify HTTPS is working (Vercel handles SSL automatically)

I'll give you screenshots-worthy step-by-step instructions when we're there.

---

## Why Vercel vs. staying on Squarespace?

For a high-ticket CGO positioning, it matters that:

- **The site loads fast** — Vercel is the fastest hosting available (edge CDN, automatic image optimization). Squarespace is slow by comparison.
- **It looks bespoke, not templated** — we control every pixel, which Squarespace fights you on.
- **It's cheap** — $0 vs. $216–$432/year for Squarespace.
- **You can evolve it** — want to add a blog, case studies, a newsletter signup, a gated download? All trivial on Vercel. Painful on Squarespace.

The only thing Squarespace gives you that we lose: a visual editor. If you want to make small content changes yourself after launch, you'd need to either (a) ask me to edit the code, (b) learn basic Markdown/git, or (c) I can set up a simple headless CMS (like Sanity or Notion-as-CMS) so you can edit content from a normal web UI without touching code. Up to you — we can decide after launch.
