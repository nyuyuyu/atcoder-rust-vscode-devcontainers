# atcoder-rust-vscode-devcontainers

Template for VS Code Dev Containers to try [AtCoder](https://atcoder.jp/) in Rust 🦀


## How to try?

In Dev Container environment you can use `atcoder` command. this is a thin-wrapper around the [cargo-compete](https://github.com/qryxip/cargo-compete) command that is specific to AtCoder.

It is used as follows.

```
# Initialize
$ atcoder init

# Login to AtCoder
$ atcoder login

# Participate in a contest
$ atcoder participate <Contest Identifier(e.g. abc086)>

# Create a package
$ atcoder new <Contest Identifier(e.g. abc086)>

# Open contest pages in your browser
$ cd <Contest Identifier(e.g. abc086)>
$ atcoder open

# Run tests
$ atcoder test

# Submit your code
$ atcoder submit
```

`atcoder` command stores [the credentials used by cargo-compete](https://github.com/qryxip/cargo-compete/blob/master/README.md#cookies-and-tokens) under your workspace.

Specifically, set `XDG_DATA_HOME` to your workspace root.
