---
title:  "GitHub Pages sitemap ping"
categories: [100DaysOfCode, Round1, Day9]
tags: [Jekyll, Sitemap, Google Webmaster Tools, Bing]
---

Added favicon and sitemap to my [personal site](https://michaeljoerg.com).

## Sitemap

My Jekyll generated sitemap now get submitted to Google and Bing on every build of my GitHub Page. Easy setup of GitHub Webhooks with the help of Simons great post [Sitemap pings for GitHub-hosted Jekyll sites](https://simonduff.net/sitemap_ping_with_github_hosted_jekyll_sites/).

Just add to web hooks to your GitHub Pages repository.

![GitHub WebHooks](/assets/images/2019/02/GitHub_WebHooks.png)

Use the following as payload urls for google

```
https://www.google.com/webmasters/tools/ping?sitemap=https://michaejoerg.com/sitemap.xml
```

and bing

```
https://www.bing.com/ping?sitemap=https://michaeljoerg.com/sitemap.xml
```

Be sure to trigger web hook on every page build

![Trigger on page build](/assets/images/2019/02/GitHub_WebHooks_Trigger_PageBuilds.png)

## Favicon

Also added simple `favicon.ico` to prevent down rating by [GTmetrix](https://gtmetrix.com) due to missing resource.

Generated full set of favicon configuration with [Favicon Generator. For real.](https://realfavicongenerator.net/) but am not sure how to modify head section of my jekyll remote theme [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/).

```html
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
<link rel="manifest" href="/site.webmanifest">
<meta name="msapplication-TileColor" content="#da532c">
<meta name="theme-color" content="#ffffff">
```