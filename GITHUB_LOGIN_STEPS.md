# GitHub Login & Authentication Steps

## Step 1: Login to GitHub in Browser

1. I've opened GitHub login page in your browser
2. Enter your GitHub username and password
3. Complete any 2FA if you have it enabled
4. You should now be logged into GitHub

## Step 2: Create Personal Access Token (Recommended)

For secure Git authentication, create a Personal Access Token:

1. Go to: https://github.com/settings/tokens
2. Click **"Generate new token"** → **"Generate new token (classic)"**
3. Give it a name: `Planning Navigator`
4. Set expiration: Choose your preference (90 days, 1 year, or no expiration)
5. Select scopes: Check **`repo`** (this gives full control of private repositories)
6. Click **"Generate token"** at the bottom
7. **IMPORTANT:** Copy the token immediately - you won't see it again!
   - It will look like: `ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`

## Step 3: Push to GitHub

After creating the token, run:

```bash
cd "/Users/tamkeen.kiani/Research Docs/Data Driven Personas/Planning-Navigator"
git push -u origin main
```

When prompted:
- **Username:** Enter your GitHub username (e.g., `Tamkeen22`)
- **Password:** Paste your Personal Access Token (not your GitHub password)

The credentials will be saved in macOS Keychain for future use.

## Alternative: Use GitHub Desktop

If you prefer a GUI:

1. Download GitHub Desktop: https://desktop.github.com/
2. Sign in with your GitHub account
3. File → Add Local Repository
4. Select: `/Users/tamkeen.kiani/Research Docs/Data Driven Personas/Planning-Navigator`
5. Click "Publish repository"

## Verify Login

To check if you're logged in:
- Visit: https://github.com
- You should see your profile/avatar in the top right

## Troubleshooting

**If push still fails:**
- Make sure you're using the Personal Access Token as the password (not your GitHub password)
- Check that the token has `repo` scope enabled
- Verify your username is correct (case-sensitive)
