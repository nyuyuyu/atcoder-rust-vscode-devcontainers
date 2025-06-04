# atcoder-rust-vscode-devcontainers

Template for VS Code Dev Containers to try [AtCoder](https://atcoder.jp/) in Rust 🦀


## How to try?

> [!WARNING]
> VS Code v1.85 and above [may automatically install the GitHub Copilot extensions](https://github.com/microsoft/vscode-docs/blob/main/remote-release-notes/v1_85.md#automatically-install-the-github-copilot-and-pull-requests-extensions) to your Dev Container.
>
> [Some contests prohibit the use of generative AI](https://info.atcoder.jp/entry/llm-rules-en), so it is recommended to disable these extensions. Disabling the extensions is required each time you build the Dev Container.

In Dev Container environment you can use `atcoder` command(`a` and `ac` is alias). this is a thin-wrapper around the [cargo-compete](https://github.com/qryxip/cargo-compete) command that is specific to AtCoder.

It is used as follows.

> [!NOTE]
> Subcommands that require authentication(e.g. `login` / `submit`) have not worked since about May 2025. This is probably due to [this change](https://atcoder.jp/posts/1456).
>
> To solve part of this problem, I created a small script called `import-cookie` in `$PATH`. Please run this script by passing the value of the `REVEL_SESSION` cookie from atcoder.jp as an argument. When doing so, don't forget to enclose the value in single quotes. You can obtain the value of `REVEL_SESSION` from your browser’s developer tools while logged in to atcoder.jp.
>
> By doing this, subcommands that require authentication will start working. However, the `submit` subcommand only works during ongoing `Rated` contests.

```console
# Login to AtCoder
atcoder login

# Participate in a contest
atcoder participate <Contest Identifier(e.g. abc086)>

# Create a package
atcoder new <Contest Identifier(e.g. abc086)>

# Open contest pages in your browser
cd <Contest Identifier(e.g. abc086)>
atcoder open

# Run the tests of A
atcoder test a

# Submit your code of A
atcoder submit a
```

`atcoder` command stores [the credentials used by cargo-compete](https://github.com/qryxip/cargo-compete/blob/master/README.md#cookies-and-tokens) under your workspace.

Specifically, `XDG_DATA_HOME` is set to the root of the workspace.
