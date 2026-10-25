# crescentiajung.com

A static site. No build step. Edit the HTML files directly.

- `index.html` is the whole site: About, Publications, Awards & Press.
- `publications/index.html` only redirects old /publications links to the main page.
- `style.css` holds all colors and layout. The four lines marked (theme) at the top set the color.
- `photo.jpg` is your portrait.

Blue theme values, if you switch: `--accent: #2f6b9a; --accent-soft: #e3f1fb; --accent-mid: #a9d3ef; --line: #dcebf5;`

## Move from Squarespace to GitHub Pages

### 1. Photo
Already included. To replace it, save a square image as `photo.jpg`.

### 2. Put the site on GitHub
1. Create a public repo named `crescentiajung.com` (any name works).
2. Upload every file in this folder, keeping `publications/` as a folder.
3. Go to Settings > Pages. Set Source to "Deploy from a branch," branch `main`, folder `/ (root)`. Save.
4. Under Custom domain, enter `www.crescentiajung.com`. The `CNAME` file already sets this.

### 3. Point the domain at GitHub (in Squarespace)
Go to Squarespace > Settings > Domains > crescentiajung.com > DNS.

1. Delete the "Squarespace Defaults" preset records.
2. Add four A records, host `@`:
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153
3. Add one CNAME record, host `www`, value `YOUR-GITHUB-USERNAME.github.io`.
4. Leave any email (MX/TXT) records alone.

### 4. Turn on HTTPS
DNS takes 15 minutes to a few hours. Back in GitHub Settings > Pages, wait for the DNS check to pass. Then tick "Enforce HTTPS."

### 5. Cancel the Squarespace website plan last
Confirm https://www.crescentiajung.com and https://crescentiajung.com both load the new site. Then cancel only the website subscription. Keep the domain registration and auto-renew on.
