<!-- README.md is generated from README.Rmd. Please edit that file -->

# animovementtemplate

<!-- badges: start -->
<!-- badges: end -->

*Template package for animovement pkgdown websites*

`animovementtemplate` holds the shared [pkgdown](https://pkgdown.r-lib.org)
configuration for every package in the [animovement](https://animovement.dev)
ecosystem — the navbar, the ecosystem dropdown, the theme, and the shared author
details — so they live in one place instead of being copied into each package.

## Usage

Each ecosystem package opts in from its own `_pkgdown.yml`:

``` yaml
template:
  bootstrap: 5
  package: animovementtemplate
```

and declares the template as a website dependency in `DESCRIPTION` so the
pkgdown build installs it:

```
Config/Needs/website: animovement/animovementtemplate
```

The package then keeps only what is genuinely package-specific in its own
`_pkgdown.yml` — `url`, the `home.title`, and the `reference` index. Everything
shared (navbar, dropdown, authors, theme) is inherited from here.

To change a shared link or add a new package to the dropdown, edit
`inst/pkgdown/BS5/_pkgdown.yml` here once; every site picks it up on its next
build.
