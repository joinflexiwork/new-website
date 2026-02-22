# Push to GitHub & Deploy on Vercel

Your site is committed locally. Follow these steps to put it on GitHub and Vercel.

---

## 1. Push to GitHub

1. **Create a new repository on GitHub**
   - Go to [github.com/new](https://github.com/new)
   - Repository name: e.g. `flexiwork-website` or `joinflexi-work`
   - Leave "Add a README" **unchecked** (you already have a repo)
   - Click **Create repository**

2. **Add the remote and push** (replace `YOUR_USERNAME` and `YOUR_REPO` with your GitHub username and repo name):

   ```powershell
   cd "C:\Users\DELL\Desktop\FlexiWork\_websites\NEW WEBSITE"
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git branch -M main
   git push -u origin main
   ```

   If your default branch is already `master`, use:

   ```powershell
   git push -u origin master
   ```

---

## 2. Deploy on Vercel

1. Go to [vercel.com](https://vercel.com) and sign in (use **Continue with GitHub**).
2. Click **Add New…** → **Project**.
3. **Import** your GitHub repo (e.g. `flexiwork-website`).
4. Vercel will detect a static site. Keep the defaults:
   - **Framework Preset:** Other
   - **Root Directory:** ./
   - **Build Command:** leave empty (static HTML)
   - **Output Directory:** leave empty
5. Click **Deploy**. Vercel will build and give you a URL (e.g. `your-project.vercel.app`).
6. (Optional) Add your custom domain **joinflexi.work** in **Project → Settings → Domains**.

---

**Optional: Vercel CLI**

To deploy from the terminal later:

```powershell
npm i -g vercel
cd "C:\Users\DELL\Desktop\FlexiWork\_websites\NEW WEBSITE"
vercel
```

Follow the prompts to log in and link the project.
