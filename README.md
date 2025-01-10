# Semantic Release for Elixir

[![Hex.pm Version](https://img.shields.io/hexpm/v/semantic_release.svg)](https://hex.pm/packages/semantic_release)
[![Hex.pm Docs](https://img.shields.io/badge/hex-docs-lightgreen.svg)](https://hexdocs.pm/semantic_release/)
[![Hex.pm Downloads](https://img.shields.io/hexpm/dw/semantic_release.svg)](https://hex.pm/packages/semantic_release)
[![Last Commit](https://img.shields.io/github/last-commit/unill-io/semantic_release.svg)](https://github.com/unill-io/semantic_release/)

Mix tasks for installing and running [`semantic-release`](https://github.com/semantic-release/semantic-release/) (and the adapter plugin [`semantic-release-hex`](https://github.com/unill-io/semantic-release-hex/)) in Elixir projects.

> **⚠️ WARNING**
>
> This is a pre-release version. As such, anything _may_ change
> at any time, the public API _should not_ be considered stable,
> and using a pinned version is _recommended_.

> **Disclaimer**: Because `semantic-release` is written in JavaScript, this package will install Node.js in your `_build/` folder upon running.
>
> See the [`nodelix` documentation](https://hexdocs.pm/nodelix/) for more information on how Node.js is installed.

## Installation

`gpg` must be available in your PATH to verify the signature of Node.js releases.

The package can be installed by adding `semantic_release` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:semantic_release, "1.0.0-alpha.9", only: :dev, runtime: false}
  ]
end
```

## Configuration

You can list additional npm packages to be passed to the `npm install` command:

```elixir
config :semantic_release,
  additional_packages: [
    "@semantic-release/changelog",
    "@semantic-release/git",
  ]
```

This can also be used to override automatically installed package versions:

```elixir
config :semantic_release,
  additional_packages: [
    "semantic-release-hex@next",
    "@semantic-release/changelog",
    "@semantic-release/git",
  ]
```

## Versioning

This project follows the principles of [Semantic Versioning (SemVer)](https://semver.org/).
