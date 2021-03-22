---
title: "Different GitHub Accounts"
date: 2021-03-22T18:47:04+01:00
draft: false
tags: ["note", "git", "github", "ssh", "problem"]
description: "Use different SSH keys for Github Accounts"
---

### Problem Description

Since I try to keep some online identities separate, I often stumble into problems like "Which email alias did I use for this service?"

This time a new problem popped up when I created a second GitHub account. I want to `git push` via SSH key and each account should have its own key (not sure why, but it feels correct).

### Solution

**Gist**: Create a ssh config file that references different keys for different hosts. One `Host` can just be the default _github.com_. The other `Host` must be matched in _~/clonedRepo/.git_

So the resulting files on my local machine look like this:

_~/ghostletters/.ssh/config_
```bash {hl_lines=[8, 11]}
# Default GitHub
Host github.com
    HostName github.com
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/id_ed25519

# ghostletters GitHub
Host ghostletters.github.com
    HostName github.com
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/id_ed25519_ghostletters
```

_~/ghostletters/clonedRepo/.git_
```bash {hl_lines=[3]}
[..]
[remote "origin"]
	url = git@ghostletters.github.com:ghostletters/clonedRepo.git
[..]
```

The part after the `@` is the same as the `Host` in the ssh config. Note the user in front of the `@` is always `git`. 

### Sources

Following resources helped me to figure it out

- [YT - How to Work with GitHub and Multiple Accounts](https://www.youtube.com/watch?v=fnSRBRiQIU8)
  - found in comment of [SO - Multiple GitHub Accounts & SSH Config](https://stackoverflow.com/questions/3225862/multiple-github-accounts-ssh-config)
  
Boom, it works.