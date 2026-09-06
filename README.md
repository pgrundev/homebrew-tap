# pgrundev/homebrew-tap

Homebrew tap for the pgrun developer tools:

| Formula | What it is |
|---|---|
| [pgbot](https://github.com/pgrundev/pgbot) | in-database observability for PostgreSQL |
| [pgterm](https://github.com/pgrundev/pgterm) | terminal UI that watches all your Postgres databases at once, powered by pgbot |
| [pgbook](https://github.com/pgrundev/pgbook) | the Postgres Book in your terminal |

```sh
brew install pgrundev/tap/pgbot
pgbot inspect "$DATABASE_URL"

# pgterm drives pgbot; name both so Homebrew trusts both from this tap
brew install pgrundev/tap/pgterm pgrundev/tap/pgbot
pgterm
```

Homebrew 6 trusts only the third-party formulae you name on the command line,
so install same-tap companions by name (as above) or run
`brew trust pgrundev/tap` once.

`Formula/pgbot.rb` and `Formula/pgterm.rb` are **generated and pushed by their
release workflows** (GoReleaser's `brews` block for pgbot, `packaging/homebrew/
formula.sh` for pgterm — each authenticated with a deploy key scoped to this
repository) on every tagged release. Do not edit them by hand — the next
release overwrites them. Downloads are the signed release archives from
[pgbot's Releases](https://github.com/pgrundev/pgbot/releases); each platform's
SHA-256 is pinned in the formula and verified by Homebrew.

Other install paths (npm, `curl | sh` with cosign verification, Docker, `go
install`, .deb/.rpm) are listed in the
[pgbot README](https://github.com/pgrundev/pgbot#install).
