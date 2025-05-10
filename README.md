# Testing-in-Go
Introduction to Testing in Go (Golang)

### installing go

- Install go from https://go.dev/doc/install
- Type to the terminal:
```bash
    go version
```
- Pressing Cmd + Shift + P (on macOS) opens the Command Palette, GO: Install/Update
- Install [go extension](https://code.visualstudio.com/docs/languages/go),
[gotemplate-syntax](https://marketplace.visualstudio.com/items/?itemName=casualjim.gotemplate)

### installing docker

- Install [docker](https://www.docker.com/)


### test files live right next to the application

1. navigate to folder

2. run go app.
```bash
    go run . 
```
3. run go test.
```bash
    go test . 
    go test -v .
```

- test has to live in a file ending in _test.go
- test usually live right beside the thing being tested
- any function that is in a file ending in _test.go will not run in test execution
- unless its name starts with Test followed by something that is not a lowercase letter

### test coverage

1. run coverage
```bash
    go test -coverprofile=coverage.out
    go test -cover . 
```

2. look at it
```bash
    go tool cover -html=coverage.out
```

3. or set up an alias for this 2
```bash
    go test -coverprofile=coverage.out && go tool cover -html=coverage.out
```
 