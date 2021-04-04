---
title: How to fix dpkg dependency problems
date: 2021-04-04 20:01:49
tags:
  - P&S
  - Linux
---
## Problem

I download and dpkg a deb file, and get error logs:

```sh
dpkg: dependency problems prevent configuration of teamviewer:
 teamviewer depends on libqt5webkit5 (>= 5.5) | qt56-teamviewer; however:
  Package libqt5webkit5 is not installed.
  Package qt56-teamviewer is not installed.
```

## Solution

dpkg assumes the user have pre-installed certain dependencies so it would not do the job for us. To fix this I use `apt-get -f install` right after the dependency err.

From the man page:

```sh
-f, --fix-broken
    Fix; attempt to correct a system with broken dependencies in place.
    This option, when used with install/remove, can omit any packages
    to permit APT to deduce a likely solution. If packages are
    specified, these have to completely correct the problem. The option
    is sometimes necessary when running APT for the first time; APT
    itself does not allow broken package dependencies to exist on a
    system. It is possible that a system's dependency structure can be
    so corrupt as to require manual intervention (which usually means
    using dpkg --remove to eliminate some of the offending packages).
    Use of this option together with -m may produce an error in some
    situations. Configuration Item: APT::Get::Fix-Broken.
```

## References

1. <https://blog.csdn.net/Teri_Tor/article/details/109328912>
