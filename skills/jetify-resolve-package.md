---
name: jetify-resolve-nix-package
description: Find a Nix package by name and resolve a specific version to an installable flake reference using the Jetify Nixhub API.
api: Nixhub API
base_url: https://search.devbox.sh/v2
operations:
- searchPackages
- getPackage
- resolvePackageVersion
generated: '2026-07-19'
method: generated
source: grounded in openapi/jetify-nixhub-openapi.yml operationIds + https://www.jetify.com/docs/nixhub/
---

# Resolve a Nix Package Version with Nixhub

Use the Jetify Nixhub API to discover a Nix package and pin an exact version for use
with Devbox or Nix. The API is public (no auth) and IP-rate-limited.

## Steps

1. **Search for the package** — call `searchPackages` (`GET /search?q=<query>`).
   Read `results[].name` to pick the exact package name.

2. **Inspect version history (optional)** — call `getPackage`
   (`GET /pkg?name=<name>`) to list `releases[]`, each with `version`,
   `platforms[]`, and `attribute_path` per platform.

3. **Resolve a version** — call `resolvePackageVersion`
   (`GET /resolve?name=<name>&version=<version>`). Use the returned
   `systems[<system>].flake_installable.ref` (`owner`/`repo`/`rev`) and
   `attr_path` to install with Nix or Devbox.

## Rules

- All three operations are read-only HTTP GET and idempotent — safe to retry.
- Send required query params: `searchPackages` needs `q`; `getPackage` needs `name`;
  `resolvePackageVersion` needs both `name` and `version`. Missing them returns HTTP 400.
- Handle HTTP 429 (per-IP rate-limit pool exhausted, replenishes 5 requests/minute) by
  backing off before retrying. See conventions/jetify-conventions.yml and
  errors/jetify-problem-types.yml.
- Errors are plain HTTP status + short message (not RFC 9457 problem+json).
