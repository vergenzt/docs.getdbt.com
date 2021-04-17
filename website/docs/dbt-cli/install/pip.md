---
title: "pip"
---

dbt is a Python module distributed on [PyPi](https://pypi.org/project/dbt/), and can be installed via `pip`. We recommend using virtual environments when installing with `pip`.

<FAQ src="install-pip-os-prereqs" />
<FAQ src="install-python-compatibility" />
<FAQ src="install-pip-best-practices" />

Once you know [which adapter](available-adapters) you're using, you can install it as `dbt-<adapter>`. For instance, if using Postgres:
```shell
pip install dbt-postgres
```
This will install `dbt-core` and `dbt-postgres` _only_:
```
$ dbt --version
installed version: 1.0.0
   latest version: 1.0.0

Up to date!

Plugins:
  - postgres: 1.0.0
```

All adapters build on top of `dbt-core`. Some also depend on other adapters: for example, `dbt-redshift` builds on top of `dbt-postgres`. In that case, you would see those adapters included by your specific installation, too.

### Upgrading

To upgrade a specific adapter plugin:
```shell
pip install --upgrade dbt-<adapter>
```
