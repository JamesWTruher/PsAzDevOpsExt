# Stages

- Init
  - `.gitignore` - needed to allow for local dev build to ignore build artifacts
  - install dependencies
    - PlatyPS
    - Pester
    - dotnet bootstrapping for binary modules
  - Provide for directory layout
    - Source
    - Output
    - Help
    - Tests
  - build script must have following hooks
    - Build
    - Test
    - Run
    - Publish ??
  - provide YML for CI
  - What-to-Do-Next.md
  - Separate yml for release pipeline

## tools/functions

- `build.ps1`
  - `New-PSProject -type [Script|Module]`
  - `Invoke-PSProjectBuild`
  - `Invoke-PSProjectTest`

eventually we would like to create a `psproject.json` which encapsulates:

- Project Metadata (module manifest contents)
- map between build artifacts and module contents and staging directory
  (we should be able to essentially `import-module <dir>` to load and test the module both during development and CI/build)


