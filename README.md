# Careerlink Kenya — Static site (ready for GitHub Pages)

This is a static site you can upload to a GitHub repository and enable GitHub Pages.
Site title: Careerlink Kenya
Owner contact: bensonmurithi2069@gmail.com
WhatsApp: 0740752615

## How to deploy
1. Create a new GitHub repository (e.g. `careerlink-kenya`).
2. Upload all files from this zip into the repository root.
3. In the repository Settings → Pages, enable Pages from the `main` branch (root).
4. Your site will be live at `https://<username>.github.io/<repo>/`.

## Images (placeholders)
Replace the placeholder images in the `images/` folder with your own files. File names used in the site:
- hero-banner.jpg
- site-logo.png
- job1.jpg
- job2.jpg
- team1.jpg
- team2.jpg

You can upload images individually to the repo (do not keep them only in an `assets` folder if you prefer them separate).

## Adding jobs
Edit `data/jobs.json`. Each job entry is an object:
```
{
  "title":"Job title",
  "category":"Mechanical",
  "location":"Nairobi",
  "deadline":"2025-10-30",
  "link":"https://apply-link",
  "excerpt":"Short description",
  "image":"images/job1.jpg"
}
```
Commit and push; GitHub Pages will rebuild the site.

## Premium verification (manual)
1. User pays via M-Pesa to 0740752615 and receives a transaction code (e.g. ABC123XYZ).
2. User submits name, email and mpesa_code via the Premium form (this uses FormSubmit to email the details to {"bensonmurithi2069@gmail.com"}).
3. Admin verifies payment in the M-Pesa till/statement.
4. Admin edits `data/premium_members.json` and adds a record:
```
{ "email":"user@example.com", "access_code":"UNIQUECODE123", "active": true, "notes":"Paid KES X on 2025-10-16, mpesa ABC123XYZ" }
```
5. Email the access code to the user. You can also create a small page or use GitHub Pages /private/ path for premium content and share link+code manually.

## Automations (optional)
To automate verification and add members automatically you can use services like Zapier/Make to listen to FormSubmit emails and update a Google Sheet or call your backend. That requires a server or automation account.

## Notes
- This is a static site; sensitive flows (real authentication, secure payment verification) require a backend or third-party automation for full security.
- If you want, I can convert this into a Jekyll collection site or create a small admin panel using Netlify + Netlify Identity.
