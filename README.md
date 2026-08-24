# skl-example-skills

Example skill package for skl. It ships one skill, hello, that greets the user.

This repo is a public example for [skl](https://github.com/ashleydavis/skilled). `skl` clones packages over SSH into `~/.skilled/store/` and symlinks each `skills/` and `commands/` tree into Cursor and Claude under a namespace.

## Install

You need [`skl`](https://github.com/ashleydavis/skilled) on your `PATH` and SSH access to GitHub.

**Project:**

```sh
skl init
skl add ashleydavis/skl-example-skills --ns demo
```

**Machine global:**

```sh
skl init -g
skl -g add ashleydavis/skl-example-skills --ns demo
```

That clones this repo to `~/.skilled/store/github.com/ashleydavis/skl-example-skills/` and links `skills/` as `demo` (for example `./.cursor/skills/demo` and `./.claude/skills/demo` in a project).

A YAML-first path that also installs this package is in [skl-example-config](https://github.com/ashleydavis/skl-example-config).

## Layout

```
skills/hello/SKILL.md
```

`hello` is a one-level skill: an immediate subdirectory of `skills/` with a `SKILL.md`. The skill description is the single-line YAML `description` in that file's frontmatter.
