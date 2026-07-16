# Switchboard Releases

Public release artifacts for **Switchboard** — a macOS cockpit for running
parallel Claude Code agents in isolated git worktrees. The source repository
is private; this repo hosts the signed, notarized builds.

## Install

**Homebrew:**

```sh
brew tap recombix/tap
brew trust recombix/tap   # newer Homebrew requires trusting third-party taps
brew install --cask switchboard
```

**Direct download:** grab the `.dmg` from the
[latest release](https://github.com/Recombix/switchboard-releases/releases/latest),
open it, and drag Switchboard to Applications.

## Requirements

macOS 12+ on Apple Silicon (arm64). Builds are signed with a Developer ID
certificate and notarized by Apple; the app updates itself automatically.
