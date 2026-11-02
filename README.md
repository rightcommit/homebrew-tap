# rightcommit Homebrew tap

Homebrew formula for [rightcommit](https://rightcommit.com): self-hosted, Rust-built
orchestration for Claude Code, Codex and Pi Agent.

Source code and documentation: [rightcommit/rightcommit](https://github.com/rightcommit/rightcommit).

## Install

```sh
brew install rightcommit/tap/rightcommit
```

On Apple Silicon Macs with macOS 15 or later, Homebrew downloads a precompiled bottle and the
install takes a few seconds. On Intel Macs and older macOS versions it compiles rightcommit,
which takes several minutes and installs Rust: afterwards `brew autoremove` removes it.

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
