# pgrundev/homebrew-tap

Homebrew tap for [pgbot](https://github.com/pgrundev/pgbot) — in-database
observability for PostgreSQL.

```sh
brew install pgrundev/tap/pgbot
pgbot inspect "$DATABASE_URL"
```

The formula in `Formula/pgbot.rb` is **generated and pushed by pgbot's release
workflow** (GoReleaser's `brews` block, authenticated with a deploy key scoped to
this repository) on every tagged release. Do not edit it by hand — the next
release overwrites it. Downloads are the signed release archives from
[pgbot's Releases](https://github.com/pgrundev/pgbot/releases); each platform's
SHA-256 is pinned in the formula and verified by Homebrew.

Other install paths (npm, `curl | sh` with cosign verification, Docker, `go
install`, .deb/.rpm) are listed in the
[pgbot README](https://github.com/pgrundev/pgbot#install).
