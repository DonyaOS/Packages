# Packages

[![MIT License](https://img.shields.io/github/license/DonyaOS/Packages?color=brightgreen)](LICENSE)
[![GitHub Linter Workflow Status](https://img.shields.io/github/workflow/status/DonyaOS/Packages/Lint?label=Linter)](#packages)
[![IRC chat on freenode](https://img.shields.io/badge/IRC%20chat%20on%20freenode-%23DonyaOS-brightgreen)](#packages)

- [Donya Package System](#donya-package-system)
- [Package Structure](#package-structure)
- [A sample package for DonyaOS](#a-sample-package-for-donyaos)
- [Submit a new package for Donya](#submit-a-new-package-for-donya)
- [Contribution to Donya](#contribution-to-donya)
- [License](#license)

## Donya Package System

The distribution employs a package system based around the concept of easily
parseable plain-text files (with fields separated by lines and spaces).

This format allows effortless interface using any programming language or just
basic UNIX utilities and tools.

## Package Structure

File name: **CATEGORY_NAME/PACKAGE_NAME/package.donya**

```
PACAKAGE_NAME/
  -package.donya
    name: "name_as_string"
    description: "description_string"
    version: "version_number_of_software_dot_allowed"
    license: "name_of_license"
    date: yyyy-mm-dd
    dependencies: []
    downloads: |
      ... link of files...
    checksums: |
      ...put your checksum for downloads file at here...
    install: |
      ...Commands...
    remove: |
      ...Commands...
```

### A sample package for DonyaOS

[**core/zlib/package.donya**](core/zlib/package.donya)

```
name: "zlib"
description: "A Massively Spiffy Yet Delicately Unobtrusive Compression Library"
version: "1.2.11"
license: "zlib"
date: 2017-01-15
dependencies: []
downloads: |
  https://zlib.net/zlib-1.2.11.tar.gz
checksums: |
  c3e5e9fdd5004dcb542feda5ee4f0ff0744628baf8ed2dd5d66f8ca1197cb1a1
install: |
  cd zlib-1.2.11
  ./configure \
    --prefix=/usr \
    --libdir=/usr/lib \
    --shared
  make
  make DESTDIR="$1" install
remove: |
  echo "Removing … "
```

### Submit a new package for Donya

Follow [Donya structure](#package-structure) carefully, then fork this repository and push your commits, and finally send Pull Request.

### Contribution to Donya

Please make sure to read the [Contributing Guide](CONTRIBUTING.md) before making a pull request. If you have a Donya-related project/feature/tool, add it with a pull request to this curated list!

Thank you to all the people who already contributed to DonyaOS!

### License

[MIT License](LICENSE)
