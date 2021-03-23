---
title: "Add Comments to Hugo Blog"
date: 2021-03-23T22:19:10+01:00
draft: false
tags: ["note", "comment", "mastodon", "javascript"]
description: "Use JavaScript to load comments from Mastodon"

comments:
  host: fosstodon.org
  username: ghost_letters
  id: 105941316911277422
---

After reading this [Toot from Surendrajat](https://fosstodon.org/web/statuses/105935391504191020) I wanted to add Mastodon Toots as comments. Thanks [@carl](https://linuxrocks.online/@carl) for inventing the smart comment solution and sharing the required JavaScript / Hugo integration.

Original source: [Adding comments to your static blog with Mastodon](https://carlschwan.eu/2020/12/29/adding-comments-to-your-static-blog-with-mastodon/)

If you want to see how it all comes together, check out these git commits
 - [add required code](https://github.com/ghostletters/blog/commit/437294d1333a6189d3e461627a92fcfdd56b3e92)
 - toot
 - [add toot ID to this post](https://github.com/ghostletters/blog/commit/6f9225a1e3f55bbb2ece5dbf721b139a7ab0cedb)


