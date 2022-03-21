[![license](https://img.shields.io/github/license/micro-os-plus/cmsis-os-xpack)](https://github.com/micro-os-plus/cmsis-os-xpack/blob/xpack/LICENSE)
[![CI on Push](https://github.com/micro-os-plus/cmsis-os-xpack/workflows/CI%20on%20Push/badge.svg)](https://github.com/micro-os-plus/cmsis-os-xpack/actions?query=workflow%3A%22CI+on+Push%22)

# A source library xPack with the CMSIS RTOS compatibility layer

This project includes files to define the CMSIS RTOS on top of µOS++.

The project is hosted on GitHub as
[micro-os-plus/cmsis-os-xpack](https://github.com/micro-os-plus/cmsis-os-xpack).

## Maintainer info

This page is addressed to developers who plan to include this source
library into their own projects.

For maintainer info, please see the
[README-MAINTAINER](README-MAINTAINER.md) file.

## Install

As a source library xPacks, the easiest way to add it to a project is via
**xpm**, but it can also be used as any Git project, for example as a submodule.

### Prerequisites

A recent [xpm](https://xpack.github.io/xpm/),
which is a portable [Node.js](https://nodejs.org/) command line application.

For details please follow the instructions in the
[install](https://xpack.github.io/install/) page.

### xpm

Note: the package will be available from npmjs.com at a later date.

For now, it can be installed from GitHub:

```sh
cd my-project
xpm init # Unless a package.json is already present

xpm install github:micro-os-plus/cmsis-os-xpack
```

When ready, this package will be available as
[`@micro-os-plus/cmsis-os`](https://www.npmjs.com/package/@micro-os-plus/cmsis-os)
from the `npmjs.com` registry:

```sh
cd my-project
xpm init # Unless a package.json is already present

xpm install @micro-os-plus/cmsis-os@latest

ls -l xpacks/micro-os-plus-cmsis-os
```

### Git submodule

If, for any reason, **xpm** is not available, the next recommended
solution is to link it as a Git submodule below an `xpacks` folder.

```sh
cd my-project
git init # Unless already a Git project
mkdir -p xpacks

git submodule add https://github.com/micro-os-plus/cmsis-os-xpack.git \
  xpacks/micro-os-plus-cmsis-os
```

## Branches

Apart from the unused `master` branch, there are two active branches:

- `xpack`, with the latest stable version (default)
- `xpack-develop`, with the current development version

All development is done in the `xpack-develop` branch, and contributions via
Pull Requests should be directed to this branch.

When new releases are published, the `xpack-develop` branch is merged
into `xpack`.

## User info

TBD

### Status

The µOS++ CMSIS RTOS v1 is fully functional.

### Limitations

Support for CMSIS RTOS v2 will be added in a later release.

### Build & integration info

To include this package in a project, consider the following details.

#### Source folders

- `src`

#### Include folders

- `include`

TODO: list the available headeres

#### Preprocessor definitions

TBD

#### Compiler options

- `-std=c++17` or higher for C++ sources
- `-std=c11` for C sources

#### C++ Namespaces

TBD

#### C++ Classes

TBD

### Known problems

- none

### Examples

TBD

### Tests

TBD

## License

The original content is released under the
[MIT License](https://opensource.org/licenses/MIT/),
with all rights reserved to
[Liviu Ionescu](https://github.com/ilg-ul/).
