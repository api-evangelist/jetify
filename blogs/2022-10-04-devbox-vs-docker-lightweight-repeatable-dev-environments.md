---
title: "Devbox vs Docker: Lightweight, repeatable dev environments without container woes"
url: "https://www.jetify.com/blog/devbox-turn-a-1000-container-script-into-10-lines"
date: "2022-10-04"
author: "Lucille Hua"
feed_url: "https://www.jetify.com/blog/rss/"
---
TLDR; At Jetify, our Docker development container initialization script used to be like this: image: ubuntu:22.04 ... # Install Go. wget --progress=bar:force:noscroll https://golang.org/dl/go1.19.linux-amd64.tar.gz -O go.tar.gz sudo tar -C /usr/local -xzf go.tar.gz echo "export PATH=$PATH:/usr/local/go/bin" >> ~/.zshrc rm go.tar.gz # Add symlinks for the binaries to be accessible in non-login sessions.
