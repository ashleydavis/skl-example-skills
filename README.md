# skl-example-skills

Example package for skl. It ships one command, `hello`, that greets the user. Claude slash-autocompletes `/demo:hello` when the namespace is `demo`.

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

That clones this repo to `~/.skilled/store/github.com/ashleydavis/skl-example-skills/` and links `commands/` as `demo` (for example `./.claude/commands/demo` in a project). In Claude, type `/demo:hello`.

A YAML-first path that also installs this package is in [skl-example-config](https://github.com/ashleydavis/skl-example-config).

## Layout

```
commands/hello.md
```

`hello` is a command: a `*.md` file under `commands/`. The description is the single-line YAML `description` in that file's frontmatter.

Docs: https://ashleydavis.github.io/skl-example-skills/
