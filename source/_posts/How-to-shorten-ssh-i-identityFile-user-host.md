---
title: How to shorten 'ssh -i identityFile user@host'
date: 2021-04-03 20:13:20
tags: 
- P&S
- AWS
---
## Problem

It feels really cumbersome to enter `ssh -i identityFile user@host` every time I connect to my vps. It's lengthy and I never remember my host ip.

## Solution

We can put all these connection details like your key, your username and of course your host into ssh's configuration file.

```sh
vim /etc/ssh/ssh_config
```

and append the following

```sh
# Lightsail
Host name-of-your-choice
HostName host
Port 22                             # 22 is default ssh port
User user
IdentityFile file
```

Ok, you can now create a connection using `ssh name-of-your-choice`

## References

1. <https://www.sohu.com/a/433733604_120161573>
2. <https://blog.csdn.net/huasonl88/article/details/52166876>