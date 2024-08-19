# nbility-model.github.io

This repository hosts the source code for the Nbility-model documentation website at <https://nbility-model.github.io>.

## Testing/previewing the documentation site locally

The documentation website is built with [mkdocs](https://www.mkdocs.org/), using the theme [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/getting-started/).

To test the documentation site locally, first clone the repository, install the package [`mkdocs-material` from PyPI](https://pypi.org/project/mkdocs-material/), and run `mkdocs serve`.
Detailed instructions [at the Material for MkDocs documentation site](https://squidfunk.github.io/mkdocs-material/creating-your-site/#previewing-as-you-write).


## Deployment

The website is deployed using [GitHub Pages](https://docs.github.com/en/pages).
Deployment is automated using [GitHub Actions](https://docs.github.com/en/actions), so that on each commit on the main branch, the website is rebuilt.
We follow the exact same steps as outlined in the [documentation on publishing your site, by Materials for MkDocs](https://squidfunk.github.io/mkdocs-material/publishing-your-site/#github-pages).

**Note**: while we use GitHub Actions for automating deployment, we *do not use* the ['deploy-pages'](https://github.com/actions/deploy-pages) action that GitHub offers.
Instead, MkDocs pushes the site to a separate branch `gh-pages` which is then used as the website root for GitHub Pages.


## Submitting feedback

On each page on the documentation website, you find the following icon on the right-hand page: 
![Edit icon](docs/images/edit-icon.png)

Pressing this button will lead you directly to the source code of the corresponding page in GitHub.
Here, you can commit a change, which you can later merge into the website by submitting a pull request.

To learn more about contributing, check out our [contributing guide](https://nbility-model.github.io/CONTRIBUTING/).

