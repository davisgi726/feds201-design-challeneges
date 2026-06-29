# FEDS 201 — Engineering Design Challenges

Mini engineering design challenges for the FEDS 201 Mechanical Design team. Each challenge is a self-contained progressive web activity — students work through 5–6 pages, answer questions, build a CAD model in Onshape, and generate a PowerPoint report. No login required. Answers persist in the browser via localStorage.

---

## Folder Structure

```
feds201-design-challenges/
│
├── index.html                          ← Landing page (start here)
│
├── challenge-01-tennis-ball/
│   └── index.html                      ← Tennis Ball Desk Holder
│
├── challenge-02-printability/
│   └── index.html                      ← Design for 3D Printability
│
├── challenge-03-cat-toy/
│   └── index.html                      ← The Cat Toy Problem (Design Process)
│
└── README.md                           ← This file
```

> **Important:** Folder and file names must match exactly — the landing page links to these paths.

---

## Challenges

| # | Title | Topics | Pages |
|---|-------|--------|-------|
| 01 | Tennis Ball Desk Holder | Stability, CoG, Contact Geometry, Onshape Assembly | 5 |
| 02 | Design for 3D Printability | FDM rules, Joint types, Pixel scaling, Cost | 5 |
| 03 | The Cat Toy Problem | Client interview, SMART requirements, Decision matrix, Prototype | 6 |

---

## Deploying to Netlify

### First-time setup (~10 minutes)

**Step 1 — Create a GitHub account**
Go to [github.com](https://github.com) and sign up with your school email.

**Step 2 — Create a new repository**
1. Click **+** → **New repository**
2. Name it: `feds201-design-challenges`
3. Set to **Public**
4. Check **Add a README file**
5. Click **Create repository**

**Step 3 — Upload all files**
1. In your new repo, click **Add file** → **Upload files**
2. Drag your entire `feds201-design-challenges` folder into the upload zone
3. GitHub will preserve the folder structure automatically
4. Add a commit message: `Initial upload — all 3 challenges`
5. Click **Commit changes**

**Step 4 — Create a Netlify account**
Go to [netlify.com](https://netlify.com) and sign up — click **Sign up with GitHub** so they're linked.

**Step 5 — Deploy from GitHub**
1. In Netlify dashboard → **Add new site** → **Import an existing project**
2. Click **GitHub** → authorize → find `feds201-design-challenges`
3. Settings: Branch = `main`, Build command = *(leave empty)*, Publish directory = `/` (root)
4. Click **Deploy site**

**Step 6 — Set your URL**
1. Go to **Site configuration** → **Change site name**
2. Set it to: `feds201-challenges` (or whatever you prefer)
3. Your permanent URL becomes: `https://feds201-challenges.netlify.app`

**Step 7 — Share with students**
Paste `https://feds201-challenges.netlify.app` into Google Classroom as a link. Students click it, the landing page opens, they pick a challenge.

---

## Updating a challenge (after initial setup)

This is the fast path — takes about 2 minutes once set up.

### Option A — GitHub web interface (no software needed)
1. Go to your repo on github.com
2. Navigate to the file you want to update (e.g. `challenge-01-tennis-ball/index.html`)
3. Click the **pencil icon** (Edit this file)
4. Make your change — or click the upload icon to replace the whole file
5. Commit changes
6. Netlify detects the change and redeploys automatically in ~60 seconds

### Option B — Claude Code (recommended for bigger updates)
1. Open **Claude Desktop** → **Code** tab
2. Open your local `feds201-design-challenges` folder
3. Tell Claude what to change — Claude edits the file directly
4. Claude runs `git add . && git commit -m "your message" && git push`
5. Netlify auto-deploys in ~60 seconds

### Option C — Drag and drop to Netlify (no GitHub needed)
1. Go to your Netlify dashboard → your site → **Deploys** tab
2. Drag your updated **folder** (not individual files) onto the deploy drop zone
3. Netlify replaces everything — same URL, instant

> ⚠️ Always drag the **whole folder**, not individual files. Dragging individual files creates a new deploy with only that file.

---

## Adding a new challenge

1. Create a new folder: `challenge-04-your-topic/`
2. Put your HTML file inside it named `index.html`
3. Update `index.html` (the landing page) — replace the "Coming Soon" card with a live card linking to `challenge-04-your-topic/index.html`
4. Upload to GitHub (or push via Claude Code)
5. Netlify deploys automatically

---

## How the challenges work

- **No server required** — everything runs in the browser
- **localStorage** saves student answers — they must use the same browser/computer each session
- **PptxGenJS** generates the PowerPoint report client-side — no upload needed
- **Onshape** links are external — students need a free Onshape Education account
- All challenges work on school Chromebooks as long as the hosting domain is accessible

---

## Troubleshooting

| Problem | Fix |
|---------|-----|
| Student answers disappeared | They used a different browser or computer. localStorage is per-browser. |
| PPTX won't download | Check that the CDN (`cdn.jsdelivr.net`) isn't blocked. The PPTX library loads from there. |
| Challenge links go to 404 | Folder name in the repo doesn't match the link in `index.html`. Check spelling exactly. |
| Site shows old version | Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac). Netlify cache clears in ~60s. |
| Netlify domain blocked by school | Try the GitHub Pages alternative — enable in repo Settings → Pages → Branch: main. URL becomes `https://yourusername.github.io/feds201-design-challenges/` |

---

## Contact

FEDS Team 201 — Rochester Hills, MI  
Built with Onshape + Claude
