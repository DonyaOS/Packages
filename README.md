# Packages

## Donya Package System

The distribution employs a package system based around the concept of easily
parseable plain-text files (with fields separated by lines and spaces).

This format allows effortless interface using any programming language or just
basic UNIX utilities and tools.

## Package Structure

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



Example:
zlib/
  -package.donya
    name: "zlib"
    description: "A Massively Spiffy Yet Delicately Unobtrusive Compression Library"
    version: "1.2.11"
    license: "zlib/libpng"
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

### Contribution

Please make sure to read the Contributing Guide before making a pull request. If you have a Donya-related project/feature/tool, add it with a pull request to this curated list!

Thank you to all the people who already contributed to DonyaOS!

### License

**MIT**
