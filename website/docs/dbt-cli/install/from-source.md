---
title: "Install from source"
id: "from-source"
---

dbt is open source software, as are almost all adapter plugins. As such, the codebases are freely available to download and build from source. To do this, you can clone the repositories from GitHub and install the local version using `pip`.

This is also an important part of contributing, if you'd like to help fix a bug or implement a sought-after feature. For more details, read the [core contributing guide](https://github.com/dbt-labs/dbt/blob/HEAD/CONTRIBUTING.md).

```shell
git clone https://github.com/dbt-labs/dbt.git
cd dbt
pip install -r requirements.txt
```

```shell
git clone https://github.com/dbt-labs/dbt-redshift.git
cd dbt-redshift
pip install .
```

<FAQ src="install-pip-os-prereqs" />
<FAQ src="install-python-compatibility" />
<FAQ src="install-pip-best-practices" />
