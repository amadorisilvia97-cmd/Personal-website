# Website deployment

The index.html file contains the website styles, scripts, embedded fonts, and main page images. Keep the assets/ folder with it: assets/tours/ contains the optimized tour catalogue images, and assets/social-preview.jpg is the social sharing preview. No build step is required.

The twelve tour entries, museum grouping, image credits, and enquiry options are generated from the shared TOUR_CATALOGUE object in index.html. Theme links use #anfrage/<tour-id>; a direct #anfrage visit defaults to an individual tour. The form prepares an email draft, including the selected tour and optional preferred date. It does not confirm a booking or send mail directly.

## GitHub Pages

In Settings → Pages, choose Deploy from a branch, main, and / (root), then Save.

## Custom domain

Configure silviaamadori.com in Settings → Pages after enabling Pages. Configure the domain DNS according to GitHub’s current documentation:
https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

For www, use a CNAME to amadorisilvia97-cmd.github.io. For the apex domain, use GitHub Pages A records or an ALIAS/ANAME supported by the DNS provider. Enable Enforce HTTPS after DNS and the certificate are ready. Verify the domain in GitHub settings where available.

The enquiry forms currently use email links. Direct form delivery and automatic confirmation require a separately configured form service; GitHub Pages has no server-side email backend. Social profile links can be added when their URLs are supplied.
