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
