# Tech by Shar Humanizing Cybersecurity Landing Page

This package is ready for GitHub Pages. It contains the landing page, all required images, and a free Google Apps Script integration that emails new requests to `info@techbyshar.net` and saves them in a Google Sheet.

## Connect the form to Google Sheets and email

1. Create a new Google Sheet. A name such as `Tech by Shar White Paper Requests` works well.
2. In the Sheet, open **Extensions**, then **Apps Script**.
3. Delete the sample function from the editor.
4. Open `google-apps-script/Code.gs` from this package and copy all of its contents into the Apps Script editor.
5. Click **Save**.
6. Click **Deploy**, then **New deployment**.
7. Select **Web app** as the deployment type.
8. Set **Execute as** to **Me**.
9. Set **Who has access** to **Anyone**.
10. Click **Deploy** and approve the Google permissions.
11. Copy the Web app URL. It should begin with `https://script.google.com/macros/s/`.
12. Open `config.js` from this package and replace `PASTE_YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE` with that URL.

The first successful submission creates a tab named `White Paper Requests`. Every submission is saved there, and a notification email is sent to `info@techbyshar.net`. The visitor's address becomes the reply address, so you can respond directly with the white paper.

## Publish with GitHub Pages

1. Create a new GitHub repository or open the repository for your Tech by Shar website.
2. Upload `index.html`, `.nojekyll`, and the `assets` folder to the repository root.
3. In GitHub, open **Settings**, then **Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select the `main` branch and the `/ (root)` folder, then click **Save**.
6. GitHub will display the public URL after deployment finishes.

## Test before sharing

Submit one test request after publishing. Confirm that a new row appears in the Google Sheet and that `info@techbyshar.net` receives the notification. Check the spam folder if the first notification does not appear in the inbox.

## Package contents

* `index.html` contains the complete landing page.
* `config.js` contains the Google Apps Script Web app URL.
* `assets/` contains the Tech by Shar logo and visual assets.
* `google-apps-script/Code.gs` contains the form backend.
* `.nojekyll` tells GitHub Pages to serve the files without Jekyll processing.
