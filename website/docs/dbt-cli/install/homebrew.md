---
title: "Homebrew"
---

### Installation

Install [Homebrew](http://brew.sh/). Then run this one-time setup:

```shell
brew update
brew install git
brew tap dbt-labs/dbt
```

Now you're ready to install dbt. Once you know [which adapter](available-adapters) you're using, you can install it as `dbt-<adapter>`. For instance, if using Postgres:
```
brew install dbt-postgres
```

Everywhere below that you see `<adapter>`, replace it with the adapter name you're using.

**Note**: While all adapter plugins maintained by dbt Labs are available on Homebrew, adapter plugins maintained by vendors and community members may not be available. In that case, we recommend you use [pip](install/pip) instead.

### Upgrading

To upgrade dbt, use:

```shell
brew update
brew upgrade dbt-<adapter>
```

### Switching versions

You can install and use multiple versions of dbt with Homebrew through something called Homebrew "links." To allow installation of another version of dbt, first unlink the current version:

```shell
brew unlink dbt-<adapter>
brew install dbt-<adapter>@0.21.0
brew link dbt-<adapter>@0.21.0
```

Now, you can use dbt version 0.21.0:

```
$ dbt --version
installed version: 0.21.0
   latest version: 0.21.0

Up to date!

Plugins:
  - bigquery: 0.21.0
  - snowflake: 0.21.0
  - redshift: 0.21.0
  - postgres: 0.21.0
```

You can switch between versions by linking the one you want to use:

```shell
brew unlink dbt-<adapter>@0.21.0
brew link dbt-<adapter>
```
