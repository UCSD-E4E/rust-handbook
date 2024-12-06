---
title: Creating Repos
slug: creating-repos
abstract: A guide to setting up a new repo in E4E.
---

## Creating the Repo
To get started creating a repo, use `cargo`. You can create a library with `cargo new --lib my-project` and an executable can be created with `cargo new --bin my-project`.

[This gitignore](https://www.toptal.com/developers/gitignore/api/rust,macos,linux,windows,visualstudiocode) provides a decent start. If you are building a binary, you want to update your `.gitignore` to commit the `cargo.lock`.

## Specifying the toolchain version
If you would like to pin the toolchain version, create a `rust-toolchain.toml` within the root of your repo. I have provided an example one below.

```
[toolchain]
# The default profile includes rustc, rust-std, cargo, rust-docs, rustfmt and clippy.
# https://rust-lang.github.io/rustup/concepts/profiles.html
profile = "default"
channel = "1.82"
```