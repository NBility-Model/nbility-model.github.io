# nbility-model.github.io

This repository hosts the source code for the NBility model documentation website at <https://nbility.netbeheernederland.nl>.

## Testing/previewing the documentation site locally

The documentation website is built with [Just the Docs](https://just-the-docs.com/).

To test the documentation site locally:

1. Clone the repository
2. Install [Ruby](https://rubyinstaller.org/)
3. Run `bundle install`
4. Run `bundle exec jekyll serve -s docs -d _site --livereload --incremental --open-url`

## Deployment

The website is deployed using [GitHub Pages](https://docs.github.com/en/pages).
Deployment is automated using [GitHub Actions](https://docs.github.com/en/actions), so that on each commit on the main branch, the website is rebuilt.
