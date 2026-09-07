# Oktoberfest & Baby Shower Website 🥨👶🍺

A festive, mobile-responsive landing page for **The Lambots' Oktoberfest & Baby Shower** in Paso Robles, CA ("Last Oktoberfest before D-Day!").

Built with pure HTML5, Tailwind CSS, and lightweight vanilla JavaScript — zero build tools, zero monthly costs, and instant load times on guests' phones.

---

## 📂 Project Structure

```text
.
├── index.html        # Main landing page (hero, Partiful link, registries, charities, FAQ)
├── assets/
│   └── invite.jpg    # High-resolution invitation flyer
└── README.md         # Deployment and domain configuration instructions
```

---

## 🚀 Step 1: Preview the Website Locally

You can preview the website right on your Mac right now:

1. Double-click `index.html` in Finder to open it in Chrome, Safari, or your default browser.
2. Or run a quick local server in your terminal:
   ```bash
   python3 -m http.server 8000
   ```
   Then open `http://localhost:8000` in your browser.

---

## 🌐 Step 2: Put it Online with GitHub Pages (100% Free)

Since you already have a GitHub account, here is how to get it live on the web in 5 minutes:

### 1. Initialize Git and Commit
Open Terminal in this folder (`/Users/steph/Documents/Oktoberfest`) and run:
```bash
git init
git add .
git commit -m "Initial commit of Oktoberfest & Baby Shower website"
git branch -M main
```

### 2. Create a Repository on GitHub
1. Go to [github.com/new](https://github.com/new).
2. Name the repository (e.g. `oktoberfest` or `oktoberfest-baby-shower`).
3. You can set it to **Public** (required for free GitHub Pages on personal accounts).
4. Click **Create repository**.

### 3. Push your Code
Copy and paste the commands GitHub gives you into your terminal:
```bash
git remote add origin https://github.com/<YOUR_GITHUB_USERNAME>/<REPO_NAME>.git
git push -u origin main
```

### 4. Enable GitHub Pages
1. In your GitHub repository, go to **Settings** (gear icon on the top right).
2. On the left sidebar under *Code and automation*, click **Pages**.
3. Under **Build and deployment > Source**, select **Deploy from a branch**.
4. Set the branch to `main` and folder to `/(root)`.
5. Click **Save**.
6. Within 1–2 minutes, your website will be live at `https://<YOUR_GITHUB_USERNAME>.github.io/<REPO_NAME>/`!

---

## 🏷️ Step 3: Connect Your Custom Domain

Your husband can point his domain to your new GitHub Pages site.

### Option A: Subdomain (e.g., `oktoberfest.yourdomain.com`) - *Recommended & Easiest!*
1. **In your GitHub Repo**:
   - Go to **Settings > Pages > Custom domain**.
   - Type in `oktoberfest.yourdomain.com` and click **Save**.
2. **In your Husband's Domain Registrar (Cloudflare, Namecheap, GoDaddy, Google/Squarespace)**:
   - Add a single **CNAME record**:
     - **Name / Host:** `oktoberfest`
     - **Target / Value:** `<YOUR_GITHUB_USERNAME>.github.io`
     - **TTL:** Automatic or 300 seconds
3. **Enable HTTPS**:
   - Back in GitHub Pages settings, check **Enforce HTTPS** (may take 10–15 minutes while the free certificate issues).

### Option B: Apex Domain (e.g., `yourdomain.com`)
1. **In your GitHub Repo**:
   - Go to **Settings > Pages > Custom domain**.
   - Type in `yourdomain.com` and click **Save**.
2. **In your Husband's Domain Registrar**:
   - Add four **A records** pointing `@` to GitHub's IP addresses:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
3. Back in GitHub Pages settings, check **Enforce HTTPS**.

---

## ✏️ Step 4: Updating Registries and Charities Later

When you finish setting up your registries and charities, updating the live site takes 30 seconds:

### Updating Baby Registries
Open `index.html` and search for:
```html
<!-- When ready, replace button with active link: <a href="YOUR_US_REGISTRY_URL" class="...">Open Registry</a> -->
<button disabled class="cursor-not-allowed ...">
  Link Coming Soon
</button>
```
Replace the disabled `<button>` with an active link to your Babylist, Target, or Amazon registry:
```html
<a href="https://www.babylist.com/..." target="_blank" rel="noopener noreferrer" 
   class="bg-beer-amber hover:bg-beer-gold text-slate-950 font-bold text-xs px-4 py-2 rounded-xl transition">
  Open US Registry
</a>
```
Do the same for the European registry!

### Updating Charities
Search for `<!-- Charity Placeholder 1 -->` in `index.html`, replace the placeholder text with your chosen charity names, descriptions, and paste their donation links into the `href="#"` tag.

### Publish Updates
Whenever you make a change, push it to GitHub:
```bash
git add index.html
git commit -m "Update baby registries and charity links"
git push
```
GitHub Pages will automatically update your live website within 30 seconds!
