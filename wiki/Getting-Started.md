## Required Software

The following items are required to build and run the services associated with the project.

### Golang
The minimum supported version of Go is `1.18`. To upgrade your installation of Go, see the [documentation](https://golang.org/doc/install).

### Staticcheck
This project uses `staticcheck` as the linter for code correctness and Go idioms. Running tests will require the use of `staticcheck`. Information on installing `staticcheck` can be found [here](https://staticcheck.io/docs).

### Go Vulnerability
This project uses `govulncheck` for vulnerability management. Running tests will require the use of `govulncheck`.
Information on installing `govulncheck` can be found [here](https://go.dev/security/vuln).

## Downloading The Project

The recommended option is to use the git clone command and clone the project anywhere on disk.

```
$ cd $HOME
$ mkdir code
$ cd code
$ git clone https://github.com/dmitryovchinnikov/blockchain
$ cd blockchain
```

## Running Tests

Navigate to the root of the project and run the test suite.

```
$ cd $HOME/code/blockchain
$ make test
```