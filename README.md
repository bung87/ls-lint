# ls-lint
ls-lint is a linter for [LiveScript](http://livescript.net/).

[![npm version][npm-img]][npm-url]
[![Dependency Status][dependency-img]][dependency-url]
[![Build Status][build-img]][build-url]
[![GitHub license][license-img]][license-url]

## Usage

### CLI

```bash
 ls-lint [options]... [file]...
```

#### options

Option              | Description
---                 | ---
-h, --help          | output usage information
-v, --version       | output the version number
-c, --config <file> | use specified configuration file

#### Priority order of configuration

1. specified configuration with `--config`
1. `ls-lint.lson` in the current directory
1. default configuration

### API

```livescript
require! 'ls-lint'

ls-lint.lint '(x, y) -> x + y'
```

#### ls-lint.lint source, [options]

Returns a list of errors, warnings.

##### options

* `config`

  Overwrites default configuration.

  ```livescript
  config:
    max-file-lines:
      level: \warning
      value: 200
      eol-last: \ignore
  ```

[npm-img]: https://badge.fury.io/js/ls-lint.svg
[npm-url]: https://badge.fury.io/js/ls-lint
[dependency-img]: https://gemnasium.com/badges/github.com/eheitherd/ls-lint.svg
[dependency-url]: https://gemnasium.com/github.com/eheitherd/ls-lint
[build-img]: https://travis-ci.org/eheitherd/ls-lint.svg?branch=master
[build-url]: https://travis-ci.org/eheitherd/ls-lint
[license-img]: https://img.shields.io/badge/license-MIT-blue.svg
[license-url]: https://raw.githubusercontent.com/eheitherd/ls-lint/master/LICENSE
