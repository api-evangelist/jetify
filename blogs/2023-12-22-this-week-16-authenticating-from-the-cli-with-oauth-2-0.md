---
title: "This Week #16: Authenticating from the CLI with OAuth 2.0"
url: "https://www.jetify.com/blog/weekly-update-16"
date: "2023-12-22"
author: "John Lago"
feed_url: "https://www.jetify.com/blog/rss/"
---
As we’ve discussed in previous issues of our Devlog, we’ve been developing a new service for securely managing environment variables and secrets alongside your Devbox shell. As part of this service, we needed a way to securely authenticate the Devbox CLI so that it can access protected resources and secrets. In this post, we’ll describe how we developed an auth flow for the CLI using the OAuth 2.0 Standard .
