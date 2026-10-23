---
title: "Creating Nix-Powered Docker Containers with Devbox"
url: "https://www.jetify.com/blog/creating-nix-powered-docker-containers-with-devbox"
date: "2023-05-17"
author: "John Lago"
feed_url: "https://www.jetify.com/blog/rss/"
---
We designed Devbox to build fast, reproducible development environments without the overhead and complexity of Docker. As described in a previous blog post , this is how we use Devbox internally — we generate a complete development environment with a devbox shell and skip the headaches of rebuilding our Docker containers when we make changes. While this works well for many use cases, we understand that developers may need to generate a Docker container to use their dev environment with their existing infrastructure or deploy to other cloud platforms.
