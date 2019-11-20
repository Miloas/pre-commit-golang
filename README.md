
pre-commit-golang
=================

golang hooks for http://pre-commit.com/

### Using these hooks

Add this to your `.pre-commit-config.yaml`

    - repo: git://github.com/dnephin/pre-commit-golang
      rev: master
      hooks:
        - id: go-fmt
        - id: validate-toml
        - id: go-unit-tests
        - id: go-build
        - id: revive

### Available hooks

- `go-fmt` - Runs `gofmt`, requires golang
- `validate-toml` - Runs `tomlv`, requires
   https://github.com/BurntSushi/toml/tree/master/cmd/tomlv
- `go-unit-tests` - run `go test -tags=unit -timeout 30s -short -v`
- `go-build` - run `go build`, requires golang
- `revive` - run `revive -config defaults.toml --formatter friendly ./...`, requires [revive](https://github.com/mgechev/revive)

### NOTICE

This project fork from `https://github.com/dnephin/pre-commit-golang`
