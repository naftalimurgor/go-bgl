# go-bgl
<img src="Icon.png" style="height: 60px;"/>

> The go-to Bitgesell Transaction (go-bgl) GoLang library  

## Table of Contents

- [Installation](#installation)
- [Documentation](#documentation)
- [Examples & Tests](#examples--tests)
- [Benchmarks](#benchmarks)
- [Code Standards](#code-standards)
- [Usage](#usage)
- [Maintainers](#maintainers)
- [Contributing](#contributing)
- [License](#license)

<br/>

## Installation

**go-bt** requires a [supported release of Go](https://golang.org/doc/devel/release.html#policy).

```shell script
go get -u github.com/naftalimurgor/go-bgl/v2
```

<br/>

## Documentation

View the generated [documentation](https://pkg.go.dev/github.com/libsv/go-bt)

[![GoDoc](https://godoc.org/github.com/libsv/go-bt?status.svg&style=flat)](https://pkg.go.dev/github.com/libsv/go-bt)

For more information around the technical aspects of Bitcoin, please see the updated [Bitcoin Wiki](https://wiki.bitcoinsv.io/index.php/Main_Page)

<br/>

### Features

- Full featured Bitcoin transactions and transaction manipulation/functionality
- Auto-fee calculations for change outputs
- Transaction fee calculation and related checks
- Interfaced signing/unlocking of transaction inputs for easy adaptation/custimisation and extendability for any use case
- Bitcoin Transaction [Script](bscript) functionality
  - Bitcoin script engine ([interpreter](bscript/interpreter))
  - P2PKH (base58 addresses)
  - Data (OP_RETURN)
  - [BIP276](https://github.com/moneybutton/bips/blob/master/bip-0276.mediawiki)


<details>
<summary><strong><code>Makefile Commands</code></strong></summary>
<br/>

View all `makefile` commands

```shell script
make help
```

List of all current commands:

```text
all                  Runs multiple commands
clean                Remove previous builds and any test cache data
clean-mods           Remove all the Go mod cache
coverage             Shows the test coverage
godocs               Sync the latest tag with GoDocs
help                 Show this help message
install              Install the application
install-go           Install the application (Using Native Go)
lint                 Run the golangci-lint application (install if not found)
release              Full production release (creates release in Github)
release              Runs common.release then runs godocs
release-snap         Test the full release (build binaries)
release-test         Full production test release (everything except deploy)
replace-version      Replaces the version in HTML/JS (pre-deploy)
tag                  Generate a new tag and push (tag version=0.0.0)
tag-remove           Remove a tag if found (tag-remove version=0.0.0)
tag-update           Update an existing tag to current commit (tag-update version=0.0.0)
test                 Runs vet, lint and ALL tests
test-ci              Runs all tests via CI (exports coverage)
test-ci-no-race      Runs all tests via CI (no race) (exports coverage)
test-ci-short        Runs unit tests via CI (exports coverage)
test-short           Runs vet, lint and tests (excludes integration tests)
uninstall            Uninstall the application (and remove files)
update-linter        Update the golangci-lint package (macOS only)
vet                  Run the Go vet application
```

</details>

<br/>

## Examples & Tests

All unit tests and [examples](examples) run via [Github Actions](https://github.com/libsv/go-bt/actions) and
uses [Go version 1.16.x](https://golang.org/doc/go1.16). View the [configuration file](.github/workflows/run-tests.yml).

Run all tests (including integration tests)

```shell script
make test
```

Run tests (excluding integration tests)

```shell script
make test-short
```

<br/>

## Benchmarks

Run the Go [benchmarks](tx_test.go):

```shell script
make bench
```

<br/>

## Code Standards

Read more about this Go project's [code standards](.github/CODE_STANDARDS.md).

<br/>

## Usage

View the [examples](examples)

<br/>

## Contributing

View the [contributing guidelines](.github/CONTRIBUTING.md) and please follow the [code of conduct](.github/CODE_OF_CONDUCT.md).

### How can I help?

All kinds of contributions are welcome :raised_hands:!
The most basic way to show your support is to star :star2: the project, or to raise issues :speech_balloon:.
You can also support this project by [becoming a sponsor on GitHub](https://github.com/sponsors/libsv) :clap:
or by making a [**bitcoin donation**](https://gobitcoinsv.com/#sponsor) to ensure this journey continues indefinitely! :rocket:

[![Stars](https://img.shields.io/github/stars/libsv/go-bt?label=Please%20like%20us&style=social)](https://github.com/libsv/go-bt/stargazers)

<br/>

## License

[![License](https://img.shields.io/github/license/libsv/go-bt.svg?style=flat&v=1)](LICENSE)
