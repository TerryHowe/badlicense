# badlicense

A test repository for validating license checkers. This project intentionally uses a non-standard or problematic license configuration to help test and verify that license compliance tools correctly identify issues.

## Usage

### As a CLI

```bash
make build
./badlicense
```

### As a Library

```go
import "github.com/TerryHowe/badlicense/pkg/greeter"

func main() {
    greeter.Hello()
}
```

## Development

```bash
make build    # Build the binary
make test     # Run tests
make fmt      # Format code
make vet      # Run static analysis
```
