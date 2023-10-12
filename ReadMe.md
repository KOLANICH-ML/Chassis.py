Chassis.py [![Unlicensed work](https://raw.githubusercontent.com/unlicense/unlicense.org/master/static/favicon.png)](https://unlicense.org/)
===============
~~![GitLab Build Status](https://gitlab.com/KOLANICH/Chassis.py/badges/master/pipeline.svg)~~
~~![GitLab Coverage](https://gitlab.com/KOLANICH/Chassis.py/badges/master/coverage.svg)~~
[![Libraries.io Status](https://img.shields.io/librariesio/github/KOLANICH/Chassis.py.svg)](https://libraries.io/github/KOLANICH/Chassis.py)
[![Code style: antiflash](https://img.shields.io/badge/code%20style-antiflash-FFF.svg)](https://codeberg.org/KOLANICH-tools/antiflash.py) 

**We have moved to https://codeberg.org/KOLANICH-ML/Chassis.py, grab new versions there.**

Under the disguise of "better security" Micro$oft-owned GitHub has [discriminated users of 1FA passwords](https://github.blog/2023-03-09-raising-the-bar-for-software-security-github-2fa-begins-march-13/) while having commercial interest in success and wide adoption of [FIDO 1FA specifications](https://fidoalliance.org/specifications/download/) and [Windows Hello implementation](https://support.microsoft.com/en-us/windows/passkeys-in-windows-301c8944-5ea2-452b-9886-97e4d2ef4422) which [it promotes as a replacement for passwords](https://github.blog/2023-07-12-introducing-passwordless-authentication-on-github-com/). It will result in dire consequencies and is competely inacceptable, [read why](https://codeberg.org/KOLANICH/Fuck-GuanTEEnomo).

If you don't want to participate in harming yourself, it is recommended to follow the lead and migrate somewhere away of GitHub and Micro$oft. Here is [the list of alternatives and rationales to do it](https://github.com/orgs/community/discussions/49869). If they delete the discussion, there are certain well-known places where you can get a copy of it. [Read why you should also leave GitHub](https://codeberg.org/KOLANICH/Fuck-GuanTEEnomo).

---

This is the library to transform a `pandas.DataFrame` into another `DataFrame` suitable for machine learning. It's my own reinvention of a ~~wheel~~ [`formulaic`](https://github.com/matthewwardrop/formulaic)![PyPI Status](https://img.shields.io/pypi/status/formulaic.svg)[![Build](https://img.shields.io/github/actions/workflow/status/matthewwardrop/formulaic/tests.yml?branch=main)](https://github.com/matthewwardrop/formulaic/actions?query=workflow%3A%22Run+Tox+Tests%22)[![docs](https://img.shields.io/github/actions/workflow/status/matthewwardrop/formulaic/publish_docs.yml?label=docs)](https://matthewwardrop.github.io/formulaic/)[![codecov](https://codecov.io/gh/matthewwardrop/formulaic/branch/main/graph/badge.svg)](https://codecov.io/gh/matthewwardrop/formulaic)[![Libraries.io Status](https://img.shields.io/librariesio/github/pydata/patsy.svg)](https://libraries.io/github/pydata/patsy), which doesn't fit my needs.

It solves the following drawbacks of patsy:
* unpredictability
 * the column names are changed in unpredictable way depending on **content** of dataframe you pass to it. You also cannot retrive the names and have to write very dirty code. Here you can retrieve columns by names.
 * The content is often shit `patsy` decides that we need it. For example it can remove a column if it finds them linearry dependent. Such matrices are not suitable to all the ML algorithms and currently there is no way to disable such a behavior.
* lack of automation - I have to do everything myself: construct expression and evaluate it.

Requirements
------------
* [`numpy`](https://github.com/numpy/numpy) ![Licence](https://img.shields.io/github/license/numpy/numpy.svg) [![PyPi Status](https://img.shields.io/pypi/v/numpy.svg)](https://pypi.org/project/numpy) [![Build status](https://github.com/numpy/numpy/actions/workflows/linux.yml/badge.svg?branch=main)](https://github.com/numpy/numpy/actions/workflows/linux.yml) [![Libraries.io Status](https://img.shields.io/librariesio/github/numpy/numpy.svg)](https://libraries.io/github/numpy/numpy) 
* [`pandas`](https://github.com/pandas-dev/pandas) ![Licence](https://img.shields.io/github/license/pandas-dev/pandas.svg) [![PyPi Status](https://img.shields.io/pypi/v/pandas.svg)](https://pypi.python.org/pypi/pandas) [![CI](https://github.com/pandas-dev/pandas/actions/workflows/unit-tests.yml/badge.svg)](https://github.com/pandas-dev/pandas/actions/workflows/unit-tests.yml) [![CodeCov Coverage](https://codecov.io/github/pandas-dev/pandas/coverage.svg?branch=master)](https://codecov.io/github/pandas-dev/pandas/) [![Conda Latest Release](https://anaconda.org/conda-forge/pandas/badges/version.svg)](https://anaconda.org/conda-forge/pandas) [![License - BSD 3-Clause](https://img.shields.io/pypi/l/pandas.svg)](https://github.com/pandas-dev/pandas/blob/main/LICENSE) [![Libraries.io Status](https://img.shields.io/librariesio/github/pandas-dev/pandas.svg)](https://libraries.io/github/pandas-dev/pandas) [![Gitter.im](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/pydata/pandas)
