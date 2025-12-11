# AGENTS.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build Commands

```bash
make build    # Build the badlicense binary
make test     # Run all tests
make fmt      # Format code with go fmt
make vet      # Run go vet for static analysis
make clean    # Remove build artifacts
make release VERSION=vX.Y.Z  # Create and push a release tag
```

## Project Overview

This is a Go project (`github.com/TerryHowe/badlicense`) using Go 1.24. The project provides both a CLI binary and importable packages.

### Package Structure

- `main.go` - CLI entry point
- `pkg/greeter` - Greeting functionality, importable by other Go projects

## Using as a Library

Other Go projects can import this module:

```go
import "github.com/TerryHowe/badlicense/pkg/greeter"

func main() {
    greeter.Hello()
}
```

## Releasing a New Version

1. Ensure all changes are committed and pushed to main
2. Run tests: `make test`
3. Run vet: `make vet`
4. Create and push the release tag:
   ```bash
   make release VERSION=vX.Y.Z
   ```
5. The Go module proxy will automatically pick up the new version. Users can then:
   ```bash
   go get github.com/TerryHowe/badlicense@vX.Y.Z
   ```
