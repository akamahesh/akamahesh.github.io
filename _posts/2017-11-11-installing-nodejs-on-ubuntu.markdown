---
layout: post
title: Installing NodeJS in ubuntu 16.40 LTS
date: 2017-11-11 00:00:00 +0300
description: Installation Guide # Add post description (optional)
img: software.jpg # Add image post (optional)
tags: [NodeJS, Ubuntu] # add tag
---

This installation guide also includes: `Linux Mint` ,`Linux Mint Debian Edition(LMDE)` ,`elementary OS` , `bash on Windows` and others.

Node.js is available from the NodeSource Debian and Ubuntu binary distributions repository (formerly Chris Lea's Launchpad PPA). Support for this repository, along with its scripts, can be found on GitHub at nodesource/distributions.

>NOTE: If you are using Ubuntu Precise or Debian Wheezy, you might want to read about running Node.js >= 6.x on older distros.

```sh
$ curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
$ sudo apt-get install -y nodejs
```



Alternatively, for Node.js 8:

```sh
$ curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
$ sudo apt-get install -y nodejs
```
Optional: install build tools

To compile and install native addons from npm you may also need to install build tools:

```sh
$ sudo apt-get install -y build-essential
```




Check out the [Nodejs Official site][nodejs-official] for more info on how to get the most out of nodejs.

[nodejs-official]: https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions
