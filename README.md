# AVR Kumar · Personal website

Stories and reflections from three decades of enterprise technology, ERP delivery and leadership. This is a plain static website (HTML, CSS and JavaScript), so it runs on GitHub Pages without any build step.

## What's in this folder

| Path | Purpose |
|---|---|
| `index.html` | The whole site: profile, experience, stories and contact |
| `css/style.css` | Design: colours, typography and layout |
| `js/main.js` | Menu, story pop-ups, collections and the optional visit counter |
| `js/config.js` | **Settings: the only file you edit to switch on visit statistics** |
| `assets/` | Photos, banner, collection thumbnails, icon and fonts |
| `404.html` | Friendly page shown for broken links |
| `.nojekyll` | Tells GitHub to publish the files exactly as they are |

## Publish the site on GitHub Pages

Everything can be done in a web browser.

1. Sign in at [github.com](https://github.com) (creating an account is free).
2. Click **+** at the top right, then **New repository**.
   - For the address `https://<your-username>.github.io`, name the repository exactly `<your-username>.github.io`.
   - For any other name, such as `website`, the address becomes `https://<your-username>.github.io/website/`.
   - Choose **Public**, leave "Add a README" unticked, and click **Create repository**.
3. On the new repository's page, click **uploading an existing file**.
4. Unzip the downloaded zip on your computer. Open the unzipped folder, select **everything inside it** (`index.html`, `404.html`, `README.md` and the `css`, `js` and `assets` folders), and drag it all onto the GitHub page. Drag the contents, not the folder itself.
5. Scroll down and click **Commit changes**.
6. Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose **main** and **/ (root)**, then click **Save**.
7. Wait a minute or two and refresh the page. GitHub shows **"Your site is live at …"** with your address.

> The hidden `.nojekyll` file may not be picked up when you drag files on some computers. That's fine: the site works without it.

### Updating the site later

Open the repository, click **Add file → Upload files**, drag in the changed files (same names replace the old ones) and click **Commit changes**. The live site updates within a minute or two.

To change the "Last updated" date in the footer, open `index.html`, click the pencil icon, search for `Last updated`, edit the date and commit.

## Switch on visit logs (optional)

GitHub Pages doesn't record visitors, so the site uses **GoatCounter**: free for personal sites, no cookies and no personal data stored.

1. Sign up at [goatcounter.com](https://www.goatcounter.com). Pick a **code**, for example `avrkumar`. Your dashboard will be at `https://avrkumar.goatcounter.com`.
2. On GitHub, open `js/config.js`, click the **pencil icon**, and put your code between the quotes:
   ```js
   goatcounterCode: "avrkumar"
   ```
   Click **Commit changes**.
3. Visit your site, then open your GoatCounter dashboard. Visits appear within a minute.

Once switched on, the footer automatically shows a short note that visits are counted anonymously.

### What you will see

- Every page visit, with date and time, country, the site the visitor came from (LinkedIn, Google and so on), browser, operating system and screen size.
- Every story a visitor opens, recorded as `story/<story-name>`, so you can see which stories are read most.

### Download the visit log

In the GoatCounter dashboard, open **Settings** and choose **Export**. Start an export to get a CSV file of every visit, which opens directly in Excel. Times in the file are in UTC; add 5 hours 30 minutes for IST.

To keep your own visits out of the numbers, use GoatCounter's settings to ignore your IP address.

To switch counting off again, empty the quotes in `js/config.js` and commit.
