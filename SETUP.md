# Getting ClariNovaPartners.com live — step by step

You've already created your GitHub account and the "ClariNova Website" repository —
nice work. Here's what's left.

You should have these files: index.html, services.html, insights.html, resources.html,
contact.html, styles.css, and an `assets` folder (with your photo, logo files and icons
inside it). Keep them all together, exactly as they are.

## 1. Upload your files to the repo you already created
- Open your "ClariNova Website" repo on GitHub
- Click "Add file" → "Upload files"
- Drag in all the files and the `assets` folder together
- Scroll down, click "Commit changes"

## 2. Connect Cloudflare Pages
- Log in to Cloudflare (where your domain already lives)
- In the left sidebar, find "Workers & Pages" → "Create" → "Pages" → "Connect to Git"
- Authorize Cloudflare to see your GitHub account, then pick the "ClariNova Website" repo
- Build settings: leave everything blank/default (this is a plain HTML site, nothing to
  build) and click "Save and Deploy"
- Cloudflare gives you a working link like `clarinova-website.pages.dev` within a minute —
  click it to check everything looks right

## 3. Point your domain at it
- Still inside that Pages project, go to "Custom domains" → "Set up a custom domain"
- Type `clarinovapartners.com` and follow the prompts
- Because your domain is already on Cloudflare, this step configures itself —
  no manual DNS records to add

Give it a few minutes, then visit clarinovapartners.com — it should show your new site.

## 4. Set up bobby@clarinovapartners.com (free)
- In Cloudflare, open your domain → "Email" → "Email Routing"
- Click "Get started", then "Create address"
- Address: `bobby` → forwards to your existing inbox (e.g. bobbykakar@hotmail.com)
- Verify the forwarding address (Cloudflare emails you a confirmation link)

Once that's confirmed, anything sent to bobby@clarinovapartners.com lands straight in
your existing inbox — no new inbox to check.

## Adding these PDFs to your already-deployed site
Your site's already live, so this is just an update, not a fresh setup:
1. Open your "ClariNova-Website" repo on GitHub
2. Click "Add file" → "Upload files"
3. Drag in the whole `assets` folder from this new zip (it now includes a
   `resources` subfolder with both PDFs)
4. Commit changes
5. Cloudflare Pages will automatically rebuild and redeploy within a minute or
   two — no need to touch Cloudflare at all

The Resources page is already wired up to link to both files, so once the
upload lands, the "Download PDF" buttons go live automatically.

## Making small edits later
Every page is a plain text file — open it on GitHub (click the file, then the pencil/edit
icon), change the text between the tags, and click "Commit changes." Cloudflare
Pages redeploys automatically within a minute or two. No coding tools needed for
text-only changes.
