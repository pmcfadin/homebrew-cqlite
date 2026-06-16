# homebrew-cqlite

Homebrew tap for the [**cqlite**](https://github.com/pmcfadin/cqlite) CLI — a
local Apache Cassandra SSTable reader that works without a running cluster.

## Install

```bash
brew install pmcfadin/cqlite/cqlite
cqlite --help
```

That single command taps this repository and installs the formula. To make the
tap explicit (e.g. before installing the bare `cqlite` name):

```bash
brew tap pmcfadin/cqlite
brew install cqlite
```

Upgrade to the latest release with:

```bash
brew upgrade cqlite
```

## What it installs

`brew install` downloads the prebuilt `cqlite` binary attached to the matching
[cqlite release](https://github.com/pmcfadin/cqlite/releases), verifies its
`.sha256` checksum, and places `cqlite` on your `PATH`. Supported platforms:

| Platform | Release asset |
|----------|---------------|
| macOS Apple Silicon | `cqlite-aarch64-apple-darwin.tar.gz` |
| macOS Intel | `cqlite-x86_64-apple-darwin.tar.gz` |
| Linux arm64 (glibc) | `cqlite-aarch64-unknown-linux-gnu.tar.gz` |
| Linux x86_64 (glibc) | `cqlite-x86_64-unknown-linux-gnu.tar.gz` |

## Maintenance

`Formula/cqlite.rb` is generated, not hand-edited. Each cqlite release tag runs
[`scripts/gen-homebrew-formula.sh`](https://github.com/pmcfadin/cqlite/blob/main/scripts/gen-homebrew-formula.sh)
from the [`update-homebrew-tap`](https://github.com/pmcfadin/cqlite/blob/main/.github/workflows/release.yml)
workflow, which refreshes the version and per-platform checksums and pushes the
result here.

## License

The cqlite project is licensed under Apache-2.0. See the
[main repository](https://github.com/pmcfadin/cqlite) for details.
