---
title: "How We Sped Up Nix Package Installs in Devbox"
url: "https://www.jetify.com/blog/how-we-sped-up-nix-package-installs-in-devbox"
date: "2024-01-12"
author: "John Lago"
feed_url: "https://www.jetify.com/blog/rss/"
---
For this week’s post, we’ll describe how we keep Devbox shells fast and performant when adding or updating new packages. This will dig into some of the Nix internals behind Devbox , but shouldn’t require a huge amount of Nix experience to follow along. How Nix Finds and Installs Packages Let's start by looking at a simple Nix flake.
