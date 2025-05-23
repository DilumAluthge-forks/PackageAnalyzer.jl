[![Build Status](https://github.com/JuliaEcosystem/PackageAnalyzer.jl/workflows/CI/badge.svg)](https://github.com/JuliaEcosystem/PackageAnalyzer.jl/actions?query=workflow%3ACI)
[![](https://img.shields.io/badge/docs-dev-blue.svg)](https://juliaecosystem.github.io/PackageAnalyzer.jl/dev/)
[![DOI](https://zenodo.org/badge/332265222.svg)](https://zenodo.org/doi/10.5281/zenodo.10835825)

# PackageAnalyzer

Package to analyze the prevalence of documentation, testing and continuous
integration in Julia packages in a given registry.

## Installation

The package works on Julia v1.10 and following versions.

To install the package, in Julia's REPL, press `]` to enter the Pkg mode and run
the command

```
add PackageAnalyzer
```

Alternatively, you can run

```julia
using Pkg
Pkg.add("PackageAnalyzer")
```

## Quick example

```julia
julia> using PackageAnalyzer

julia> analyze("Flux")
Package Flux:
  * repo: https://github.com/FluxML/Flux.jl.git
  * uuid: 587475ba-b771-5e3f-ad9e-33799f191a9c
  * is reachable: true
  * Julia code in `src`: 5496 lines
  * Julia code in `test`: 2432 lines (30.7% of `test` + `src`)
  * documentation in `docs`: 1533 lines (21.8% of `docs` + `src`)
  * documentation in README: 10 lines
  * has license(s) in file: MIT
    * filename: LICENSE.md
    * OSI approved: true
  * number of contributors: 159 (and 7 anonymous contributors)
  * number of commits: 3794
  * has `docs/make.jl`: true
  * has `test/runtests.jl`: true
  * has continuous integration: true
    * GitHub Actions
    * Buildkite

```

See the [docs](https://JuliaEcosystem.github.io/PackageAnalyzer.jl/dev/) for more!

## Talks and blog posts

Check out our JuliaCon 2023 talk:

[![](https://img.youtube.com/vi/KfQTFVtZTYY/0.jpg)](https://youtu.be/KfQTFVtZTYY)

The Pluto notebook demos from that talk are available [here](https://github.com/ericphanson/PackageAnalyzerJuliaCon2023).

See also our [2021 JuliaCon talk](https://www.youtube.com/watch?v=9YWwiFbaRx8) and [associated blog post](https://julialang.org/blog/2021/08/general-survey/).

## License

The `PackageAnalyzer.jl` package is licensed under the MIT "Expat" License.  The
original author is Mosè Giordano.
