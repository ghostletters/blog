---
title: "Create WebHooks with Caddy"
date: 2021-04-04T19:10:04+01:00
draft: false
tags: ["note", "caddy", "webhook", "xcaddy", "exec"]
description: "Trigger bash script via URL"
---

### WebHook == Run Some Command

A webhook is a an HTTP endpoint that triggers 'some action'. The action will be specific for the application that provides the endpoint. In my case the action/endpoint will update my blog. Let's ignore for a moment how exactly 'updating the blog' works, and just pretend I want to execute some arbitrary command on my server as soon as I call some *very specific* URL.

### Run Commands with Caddy 'Exec' Module

The [Exec Module](https://caddyserver.com/docs/modules/exec) (for some reason caddy calls plugins 'modules') allows to bind a *path* to a command. So a config in the [caddyfile](https://caddyserver.com/docs/quick-starts/caddyfile) like

```
example.com

exec /createFile touch /home/user/new_file.txt
```

would create an empty file on the server when someone calls `example.com/createFile`. Instead of creating a file we could run any series of command line tools.

### They Said It Would Be Easy

The final result and how my workflow looks is already sketched in this [note](https://blog.ghostletters.xyz/notes/2020/4/2/1510/). While I imagined it to be pretty straight forward, it took me several hours in the end to put it together. In case you are not familar with the term *yak shaving* I highly recommend to read [Don't Shave That Yak!](https://seths.blog/2005/03/dont_shave_that/). Spoiler ahead, I did shave that yak!

So what happened? Luckily, I took notes while implementing the solution. This is how they look

- want to use [Exec module](https://caddyserver.com/docs/modules/exec) for webhook for hugo
- 'Exec' requires to custom build caddy with [xcaddy](https://github.com/caddyserver/xcaddy)
- xcaddy requires Go 1.14, but Ubuntu 20.04 repo has just 13.8
  - add official Golang repo
- 'exec' module has a [bug in the current version](https://github.com/abiosoft/caddy-exec/issues/9)
  - since I did not understand the workaround, I installed an older version

```bash
# create a new 'caddy' binary with 'exec' module
xcaddy build --with github.com/abiosoft/caddy-exec@8d34c546e3f0aa43ba803955e7d5dd2bc7bb3780
```

- had to refreseh my memory [how to configure caddy as service](https://caddyserver.com/docs/install#linux-service). This also defines where the config file is located
  - start server with: `sudo systemctl start caddy`
- back to https://caddyserver.com/docs/modules/exec or better https://github.com/abiosoft/caddy-exec
  - update caddy config

```bash
ghostletters.xyz {
  route {
    # update hugo blog
    exec /<long secret path> sh /home/caddy/refresh_blog.sh
    
    # for all other pathes redirect to blog
    redir https://blog.ghostletters.xyz{uri}
  }
}
```

- reload config: $ sudo systemctl reload caddy

- install git & hugo on server. Create `refresh_blog.sh` script

```bash
#!/bin/sh
set -xe

cd /home/user/github/blog
git pull

hugo --destination /home/caddy/blog

touch /home/user/blog_refreshed.txt      # optional
```
So most of the time I struggled with installing the Exec module. I encountered some weird behaviour where I could run the script, but when caddy executed the same script, the `cp` (copy) command produced some `read only file-system` errors. Anyway, in the end it worked and now my Hugo-based blog updates in less than 1 seconds.

Happy Easter.

