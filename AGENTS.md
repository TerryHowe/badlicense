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

This is a Go project (`github.com/TerryHowe/badlicense`) using Go 1.24. The project currently consists of a single `main.go` entry point. The Makefile handles all build, test, and release workflows.
