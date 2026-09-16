# GitHub Actions Central

Central repository for reusable GitHub Actions workflows across the Web Analytics & Event Tracking platform.

## Available Workflows

### 1. `js-tag-ci.yml`
Reusable CI workflow for client JavaScript tags:
- Setup Node.js & dependencies
- Code style & lint check
- Test execution
- Bundle build and minification
- Gzip bundle size limit validation (< 5 KB)
- Artifact upload

### 2. `rust-wasm-ci.yml`
Reusable CI workflow for Rust WebAssembly microservices:
- Toolchain setup (`wasm32-wasip1`) & caching
- Formatting (`cargo fmt`) & Linting (`cargo clippy`)
- Host unit tests
- Release WASM compilation
- Binary optimization with `wasm-opt`
- Size budget verification (< 3 MB)
- Artifact upload

### 3. `release-wasm-oci.yml`
Reusable OCI publication workflow:
- Packages compiled `.wasm` into OCI registry (GHCR) using ORAS
- Attaches WASM artifact layer media type
