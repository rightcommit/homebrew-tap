# rightcommit Homebrew tap

Homebrew formula for [rightcommit](https://rightcommit.com): self-hosted, Rust-built
orchestration for Claude Code, Codex and Pi Agent.

Source code and documentation: [rightcommit/rightcommit](https://github.com/rightcommit/rightcommit).

## Install

```sh
brew install rightcommit/tap/rightcommit
```

Homebrew compiles rightcommit on your Mac, so the first install takes several minutes.
Homebrew also installs Rust, which it keeps to build future upgrades. If you already use
[rustup](https://rustup.rs), run `brew unlink rust` once, so that your rustup toolchain stays
first.

## Start

```sh
mkdir -p ~/rightcommit && cd ~/rightcommit
rightcommit setup
rightcommit
```

`rightcommit setup` downloads the agents (Codex, Claude Code, Pi) once. Then open
<http://localhost:8080> and create the first account: it becomes the administrator.
Always start from the same folder: your data lives in its `data` subfolder.

## Update

```sh
brew update && brew upgrade rightcommit
cd ~/rightcommit && rightcommit setup
```

## Uninstall

```sh
brew uninstall rightcommit
brew untap rightcommit/tap
```

Your data stays in `~/rightcommit`. Delete that folder to remove it too.

## Problems

Open an issue in [rightcommit/rightcommit](https://github.com/rightcommit/rightcommit/issues).
