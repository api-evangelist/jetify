---
title: "Don't Rebuild Yourself - an Intro to Nix Package Caches"
url: "https://www.jetify.com/blog/dont-rebuild-yourself-an-intro-to-nix-package-caches"
date: "2024-07-12"
author: "John Lago"
feed_url: "https://www.jetify.com/blog/rss/"
---
In previous blog posts, we’ve talked about how we speed up Devbox installs by fetching package closures directly from the official Nix Cache. This blog post will dig a bit more into how a Nix cache solution works, and how it can speed up your package installation time. In addition to covering the official Nix cache, we’ll talk about how you can integrate the Jetify Cache with Devbox to speed up your shells and share your custom packages across your team.
