---
title: "Deploy Page via Github Action"
date: 2021-03-22T20:30:21+01:00
draft: false
tags: ["note", "github", "deploy", "rsync"]
description: "Deploy a static page via Github Action"
---

How I deploy my blog. Just dropping the link to the tutorial here, because the original article already explains it in great details.

[Deploy a static site with GitHub Actions](https://zartman.xyz/blog/gh-static-deploy/)

All thanks to [zartman.xyz](zartman.xyz)

### Notes to Future Me

Have 2 _secrets_ in the github blog repo:
- `DEPLOY_KEY` - this is the private key of the server
- `KNOWN_HOSTS` - in my case it is the output of 

```bash
ssh-keyscan ghostletters.xyz
# prints many lines. copy them all
```

