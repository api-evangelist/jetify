---
title: "How We Built Devbox's Package-Version Search"
url: "https://www.jetify.com/blog/how-nixhub-searches-nixpkgs"
date: "2023-08-08"
author: "Greg Curtis"
feed_url: "https://www.jetify.com/blog/rss/"
---
Back when we first released Devbox , one of the most requested features was the ability to install specific versions of packages. This isn't something that Nix easily supports out of the box, so initially Devbox could only install the most recent versions of a package. That changed in Devbox v0.5 which added a devbox search command that allows users to find and install old versions of any package.
