# How to Upload This Project to GitHub

**For first-time GitHub users** — Step-by-step guide to get your pitch deck on GitHub.

---

## Prerequisites

### 1. Create a GitHub Account (if you don't have one)
1. Go to [github.com](https://github.com)
2. Click "Sign up"
3. Follow the registration steps
4. Verify your email

### 2. Check if Git is Installed
Open Terminal and run:
```bash
git --version
```

**If you see a version number** (e.g., `git version 2.39.0`):
- ✅ You're good to go! Skip to "Upload Steps" below

**If you see "command not found"**:
- Install Git: Run this in Terminal:
  ```bash
  xcode-select --install
  ```
- Click "Install" when prompted
- Wait for installation to complete (5-10 minutes)
- Run `git --version` again to verify

---

## Upload Steps

### Step 1: Initialize Git in Your Project

Open Terminal and navigate to your project folder:
```bash
cd /Users/dlee/lockton-pitch-copy
```

Initialize git:
```bash
git init
```

You should see: `Initialized empty Git repository in /Users/dlee/lockton-pitch-copy/.git/`

---

### Step 2: Stage All Files

Add all files to git:
```bash
git add .
```

Check what will be committed:
```bash
git status
```

You should see a list of green files (all your project files).

---

### Step 3: Make Your First Commit

Create your first commit:
```bash
git commit -m "Initial commit: SonderMind pitch deck template"
```

You should see a summary of files added.

---

### Step 4: Create a New Repository on GitHub

1. Go to [github.com](https://github.com)
2. Click the **"+"** icon in top-right → **"New repository"**
3. Fill in:
   - **Repository name**: `sondermind-pitch-deck` (or any name you want)
   - **Description**: "Templatized pitch deck for SonderMind Total Brain Solutions"
   - **Visibility**:
     - ⚠️ Choose **"Private"** for confidential internal use
     - Or **"Public"** if approved for external sharing
   - **DO NOT** check "Add a README" (we already have one)
   - **DO NOT** add .gitignore or license (we have these)
4. Click **"Create repository"**

---

### Step 5: Connect Your Local Project to GitHub

GitHub will show you instructions. Copy the commands that look like this (but with YOUR username/repo):

```bash
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
git branch -M main
git push -u origin main
```

**Example** (replace with your actual username and repo name):
```bash
git remote add origin https://github.com/dlee/sondermind-pitch-deck.git
git branch -M main
git push -u origin main
```

Run these commands in Terminal (still in the `/Users/dlee/lockton-pitch-copy` folder).

---

### Step 6: Enter Your GitHub Credentials

When prompted:
- **Username**: Your GitHub username
- **Password**: ⚠️ **NOT** your GitHub password!
  - You need a **Personal Access Token** (PAT)
  - See "Creating a Personal Access Token" section below

---

### Step 7: Verify Upload

After the push completes, refresh your GitHub repository page in the browser.

You should see all your files:
- ✅ index.html
- ✅ README.md
- ✅ HANDOFF.md
- ✅ CLIENT-SETUP.md
- ✅ All images and logos

---

## Creating a Personal Access Token (PAT)

GitHub requires a PAT instead of your password for command-line access.

### Steps:
1. Go to [github.com/settings/tokens](https://github.com/settings/tokens)
2. Click **"Generate new token"** → **"Generate new token (classic)"**
3. Fill in:
   - **Note**: "Command line access for pitch deck repo"
   - **Expiration**: Choose 90 days (or longer)
   - **Scopes**: Check the **"repo"** checkbox (this selects all repo permissions)
4. Click **"Generate token"** at the bottom
5. **⚠️ COPY THE TOKEN NOW** — you can't see it again!
   - It looks like: `ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`
6. Save it somewhere secure (password manager)
7. Use this token as your "password" when git asks

---

## Making Future Updates

Once uploaded, to push new changes:

```bash
cd /Users/dlee/lockton-pitch-copy

# Check what changed
git status

# Stage all changes
git add .

# Commit with a message describing what you changed
git commit -m "Updated employee count and case study for Lockton"

# Push to GitHub
git push
```

---

## Optional: Enable GitHub Pages (Live Website)

Want your deck to be viewable as a live website?

1. Go to your GitHub repo
2. Click **Settings** tab
3. Click **Pages** in left sidebar
4. Under "Source":
   - Select **"Deploy from a branch"**
   - Branch: **main**
   - Folder: **/ (root)**
5. Click **Save**
6. Wait 1-2 minutes
7. Your deck will be live at:
   ```
   https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
   ```

**Example**: `https://dlee.github.io/sondermind-pitch-deck/`

**⚠️ Note**: Only enable GitHub Pages if this is a PUBLIC repo! Private repos can use Pages but may have restrictions.

---

## Troubleshooting

### "Permission denied"
- Make sure you're using your Personal Access Token, not your password
- Check that the token has "repo" scope

### "Repository not found"
- Verify the repository URL is correct
- Check that you have access to the repository
- Make sure you typed your username correctly

### Files missing after upload
- Check your `.gitignore` file — it may be excluding files
- Run `git status` to see what's being tracked

### "Nothing to commit"
- You haven't made any changes since your last commit
- This is fine! No need to commit if nothing changed

---

## Summary: Quick Command Reference

```bash
# First time setup
cd /Users/dlee/lockton-pitch-copy
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git branch -M main
git push -u origin main

# Future updates
git add .
git commit -m "Description of changes"
git push
```

---

## Need More Help?

- **GitHub Docs**: [docs.github.com/en/get-started](https://docs.github.com/en/get-started)
- **Git Basics**: [git-scm.com/book/en/v2/Getting-Started-About-Version-Control](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)
- **Personal Access Tokens**: [docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)

---

**You're ready to go!** 🚀
