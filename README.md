
# Self-Hosted Landing Page (GitHub Pages)

This is a simple, good-looking landing page with:
- A Microsoft Forms embed (swap in your share link)
- A fallback HTML form that posts to Formspree (or your own endpoint)
- A Thank You page
- Clean CSS, responsive layout, VAT disclaimer in footer

## Quick Start

1) Replace the Microsoft Forms URL:
   - Edit `index.html`
   - Find `FORM_URL` and paste your Microsoft Forms share link (Embed -> iframe URL works too).

2) (Optional) Use Formspree fallback:
   - Create a free form at https://formspree.io/
   - Replace `https://formspree.io/f/your-form-id` with your own endpoint in `index.html`.

3) Deploy to GitHub Pages:
   - Create a new repo (e.g. `landing-page-campaign`)
   - Upload all files in this folder to the repo root (including `.nojekyll`)
   - Go to Settings -> Pages -> Source -> Deploy from `main`
   - Wait for the green check, your site goes live.
   - (Optional) Add your custom domain in Settings -> Pages and edit the `CNAME` file to match.

4) Drip Emails (Microsoft 365):
   - In Power Automate, create a flow:
     - Trigger: When a new response is submitted (Microsoft Forms)
     - Action: Get response details
     - Action: Send an email (V2)
     - Action: Delay (e.g., 3 days)
     - Action: Send next email
   - Repeat to build your sequence.

## Customise

- Replace `assets/hero.jpg` with your Canva export or brand photo.
- Edit `assets/styles.css` for colors, sizes, spacing.
- The VAT disclaimer appears in the footer and under the form.

## Notes

- If you don't want the fallback form visible, delete the `<form id="fallbackForm">...</form>` block.
- For POPIA compliance, ensure your privacy statement is linked in the footer and that you only collect necessary data.


---

## Canva Design

Your Canva design: https://www.canva.com/design/DAG1Cv2PzZg/ORummbKgjHiyXEnhqRjWzg/edit
Export your hero/cover from Canva (JPG/PNG) and replace `assets/hero.jpg`.
You can also add more sections in `index.html` to mirror the Canva layout.
