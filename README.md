# Champlain Analytics

**champlainanalytics.ca** — Independent research for the Canadian investor.

## Structure

```
champlainanalytics/
├── index.html                          → champlainanalytics.ca (home)
├── CNAME                               → custom domain config
├── northern-bearing/
│   ├── index.html                      → champlainanalytics.ca/northern-bearing/
│   └── issue-01/
│       └── index.html                  → champlainanalytics.ca/northern-bearing/issue-01/
```

## Adding a new issue each week

1. Duplicate the `issue-01` folder → rename to `issue-02`
2. Replace the `index.html` inside with the new issue HTML
3. Open `northern-bearing/index.html` and add a new card to the issue grid (copy the existing card, update the number, date, headline, summary, and href)
4. Commit and push — GitHub Pages deploys automatically within ~60 seconds

## Setup Instructions (first time)

### 1. Create the GitHub repository
- Go to github.com → New repository
- Name it exactly: `champlainanalytics` (or your GitHub username if that's what you want)
- Set to **Public**
- Do NOT initialize with a README (you have one already)

### 2. Push this folder to GitHub
Open Terminal and run:

```bash
cd /path/to/champlainanalytics
git init
git add .
git commit -m "Launch: Northern Bearing Issue 01"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/champlainanalytics.git
git push -u origin main
```

### 3. Enable GitHub Pages
- Go to your repo on GitHub
- Settings → Pages
- Source: **Deploy from a branch**
- Branch: **main** / **/ (root)**
- Click Save

### 4. Connect your custom domain
In your repo Settings → Pages → Custom domain:
- Enter: `champlainanalytics.ca`
- Click Save
- Check "Enforce HTTPS" once it appears

### 5. Point your domain to GitHub Pages
At your domain registrar (Namecheap, Google Domains, etc.), add these DNS records:

**A Records** (point @ to GitHub):
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**CNAME Record**:
```
www → YOUR_USERNAME.github.io
```

DNS changes take 10 minutes to 48 hours to propagate. GitHub Pages will show a green checkmark when the domain is verified.

### 6. You're live
- `champlainanalytics.ca` → home page
- `champlainanalytics.ca/northern-bearing/` → archive
- `champlainanalytics.ca/northern-bearing/issue-01/` → Issue 01

---

*Not financial advice. For informational purposes only.*
