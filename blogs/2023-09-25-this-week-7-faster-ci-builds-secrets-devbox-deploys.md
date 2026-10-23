---
title: "This Week #7: Faster CI Builds, Secrets, Devbox Deploys"
url: "https://www.jetify.com/blog/this-week-7"
date: "2023-09-25"
author: "John Lago"
feed_url: "https://www.jetify.com/blog/rss/"
---
Lucille Rolled out a fresh version of the devbox-installer GitHub action to address issues and questions on Discord. This v0.7.0 update tackles Nix caching problems on both Linux and macOS. I had to do some serious detective work, as there were loads of open issues about the action/cache’s lack of sudo permissions.
