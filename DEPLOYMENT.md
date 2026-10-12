# Website deployment

The index.html file is the complete website, with embedded images, fonts, styles, and scripts. No build step is required.

## GitHub Pages

In Settings → Pages, choose Deploy from a branch, main, and / (root), then Save.

## Custom domain

Configure silviaamadori.com in Settings → Pages after enabling Pages. Configure the domain DNS according to GitHub’s current documentation:
https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

For www, use a CNAME to amadorisilvia97-cmd.github.io. For the apex domain, use GitHub Pages A records or an ALIAS/ANAME supported by the DNS provider. Enable Enforce HTTPS after DNS and the certificate are ready. Verify the domain in GitHub settings where available.

The enquiry forms currently use email links. Direct form delivery and automatic confirmation require a separately configured form service; GitHub Pages has no server-side email backend. Social profile links can be added when their URLs are supplied.
