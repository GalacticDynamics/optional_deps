<h1 align='center'> optional_dependencies </h1>
<h2 align="center">Construct Checks for Optional Dependencies</h2>

## Installation

[![PyPI platforms][pypi-platforms]][pypi-link]
[![PyPI version][pypi-version]][pypi-link]

<!-- [![Conda-Forge][conda-badge]][conda-link] -->

```bash
pip install optional_dependencies
```

## Documentation

This package allows for easy construction of checks for optional dependencies.
As every Python project can have its own unique set of optional dependencies,
`optional_dependencies` provides an
[`enum.Enum`](https://docs.python.org/3/library/enum.html) base class for
enumerating the optional dependencies.

```python
from optional_dependencies import OptionalDependencyEnum, auto

# Note that `auto` is just a re-export of enum.auto


class OptDeps(OptionalDependencyEnum):
    PACKAGING = auto()


OptDeps.PACKAGING
# <OptDeps.PACKAGING: <Version('...')>>

OptDeps.PACKAGING.is_installed
# True

OptDeps.PACKAGING.version
# <Version('...')>
```

## Citation

[![DOI][zenodo-badge]][zenodo-link]

If you found this library to be useful and want to support the development and
maintenance of lower-level code libraries for the scientific community, please
consider citing this work.

## Development

[![codecov][codecov-badge]][codecov-link]
[![Actions Status][actions-badge]][actions-link]

We welcome contributions!

<!-- prettier-ignore-start -->

[actions-badge]:            https://github.com/GalacticDynamics/optional_dependencies/workflows/CI/badge.svg
[actions-link]:             https://github.com/GalacticDynamics/optional_dependencies/actions
[codecov-badge]:            https://codecov.io/gh/GalacticDynamics/optional_deps/graph/badge.svg
[codecov-link]:             https://codecov.io/gh/GalacticDynamics/optional_deps
[pypi-link]:                https://pypi.org/project/optional_dependencies/
[pypi-platforms]:           https://img.shields.io/pypi/pyversions/optional_dependencies
[pypi-version]:             https://img.shields.io/pypi/v/optional_dependencies
[zenodo-badge]:             https://zenodo.org/badge/DOI/10.5281/zenodo.13738124.svg
[zenodo-link]:              https://zenodo.org/doi/10.5281/zenodo.13738123

<!-- prettier-ignore-end -->
