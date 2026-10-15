# Website deployment

The index.html file contains the website styles and scripts. Keep the entire assets/ folder with it: assets/images/ holds optimized WebP images, assets/icons/ the SA favicons, assets/fonts/ self-hosted fonts and OFL licenses, assets/museums/ and assets/tours/ museum and catalogue images, and assets/social-preview.jpg the sharing preview. No build step is required. The portable Silvia-Amadori-share.html remains a separate local, self-contained output and should not be uploaded as a duplicate entry point.

The twelve tour entries, museum grouping, image credits, and enquiry options are generated from the shared TOUR_CATALOGUE object in index.html. Theme links use #anfrage/<tour-id>; a direct #anfrage visit defaults to an individual tour. The form prepares an email draft, including the selected tour and optional preferred date. It does not confirm a booking or send mail directly.

## GitHub Pages

In Settings → Pages, choose Deploy from a branch, main, and / (root), then Save.

## Custom domain

Configure silviaamadori.com in Settings → Pages after enabling Pages. Configure the domain DNS according to GitHub’s current documentation:
https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

For www, use a CNAME to amadorisilvia97-cmd.github.io. For the apex domain, use GitHub Pages A records or an ALIAS/ANAME supported by the DNS provider. Enable Enforce HTTPS after DNS and the certificate are ready. Verify the domain in GitHub settings where available.

The enquiry forms currently use email links. Direct form delivery and automatic confirmation require a separately configured form service; GitHub Pages has no server-side email backend. LinkedIn and Instagram profile links are configured in the shared footer.

## Review before publication

The business postal address is still missing from the Impressum; do not describe the legal pages as complete. Photographer, museum and portrait permissions remain pending and must be confirmed before treating the supplied photos as cleared. Cloudflare is currently DNS-only, not an HTTP proxy; update privacy disclosures before changing that. Add https://silviaamadori.com/#impressum to Instagram after the address is completed. Projekte stays hidden pending finished content. Recheck the Neue Pinakothek reopening status before future content updates or confirming tours.

## Brevo newsletter

The newsletter uses a locally styled HTML form and Ajax POST to the exact public Brevo action supplied by the owner. It sends EMAIL, locale and the empty email_address_check honeypot using FormData with credentials omitted. No API keys, external Brevo scripts or iframe are loaded. Submission stays on the website and only an HTTP-success response with JSON success === true reveals the styled confirmation. The neutral confirmation says the sign-up was received and conditionally mentions a confirmation email; it does not assert double opt-in is complete.

A success:false response keeps the editable form and shows an error. Network failures, timeouts, non-JSON or ambiguous responses never claim success; the site says the result could not be verified and offers the hosted Brevo form. It does not automatically retry a request that may have already been accepted. Empty-email validation against the actual endpoint returned a readable rejection from the local browser, confirming CORS response access; no real subscriber was created. Local simulations cover success, rejection, malformed response, connection failure and timeout. A complete live success subscription was not repeated because the owner already reported a successful Brevo response.

Confirm double opt-in, consent records, unsubscribe behavior, data-processing terms, tracking settings and confirmation emails in the Brevo account. If CAPTCHA or the form fields change later, use the corresponding supported Brevo integration and verify the endpoint contract. Tour requests still prepare an email draft and are independent of Brevo.

Booking dropdown titles, museum groups and the Neue Pinakothek location notice now switch between DE, EN and IT while retaining the same tour IDs and selected value. The themed catalogue itself retains its German titles and descriptions. The native desktop select and custom mobile picker share these translated booking labels.
