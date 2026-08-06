<div align="center">

<img src="assets/switchboard-logo.png" alt="Switchboard" width="128">

# Switchboard

**Stop running one Claude Code agent at a time.**

Switchboard is a macOS cockpit for running a whole team of coding agents in
parallel — each on its own branch, in its own git worktree, never treading on
another's toes.

[**Download the latest release**](https://github.com/Recombix/switchboard-releases/releases/latest) ·
[Install](#install) · [Requirements](#requirements)

</div>

---

## One agent is a bottleneck

You give Claude a task. You wait. You give it the next one. Meanwhile four other
things on your list sit untouched, because a second agent in the same checkout
would trample the first.

Switchboard fixes the checkout problem, and then builds a cockpit around it.
Every task gets a real git worktree on a real branch. Five agents can be
mid-refactor at once, and none of them can see — or break — each other's work.

## What you get

**Genuine isolation.** One branch, one worktree, one agent. No stashing, no
"wait, who changed this file?", no half-finished work bleeding between tasks.

**The whole fleet at a glance.** Live status on every agent — which are working,
which are blocked and waiting on you, which have finished and want reviewing.

**Review without leaving.** A built-in diff view for each agent's changes, plus
its terminal tabs, right where the session is running.

**Worktrees that arrive ready.** Drop a `.switchboard/config.json` in your repo
and every new worktree sets itself up the same way: install commands, the
`.env` files git never tracked, dev-server tabs already running, the architecture
doc already open.

**Agents that know where they are.** Switchboard hands each session its own MCP
tools, so an agent can look up its task, its pull request, and what its siblings
are touching — instead of guessing from the branch name.

## Install

**Homebrew** — the easy path, and you get updates with it:

```sh
brew tap recombix/tap
brew trust recombix/tap   # newer Homebrew requires trusting third-party taps
brew install --cask switchboard
```

**Direct download** — grab the `.dmg` from the
[latest release](https://github.com/Recombix/switchboard-releases/releases/latest),
open it, and drag Switchboard to Applications.

Either way, the app keeps itself up to date from there.

## Requirements

macOS 12 or later on Apple Silicon (arm64). Every build is signed with a
Developer ID certificate and notarised by Apple, so it opens without a
right-click-to-open dance.

## About this repository

This repo hosts the signed, notarised builds and nothing else — the Switchboard
source lives in a private repository. Releases are published here as GitHub
Releases; if something looks wrong with a build, the
[issues](https://github.com/Recombix/switchboard-releases/issues) are the place
to say so.
