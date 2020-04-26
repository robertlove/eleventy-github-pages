# Eleventy on GitHub Pages

An attempt to get [Eleventy](https://www.11ty.dev/) running on [GitHub Pages](https://pages.github.com/) with the same amount of effort as it takes to get [Jekyll](https://jekyllrb.com/) to do the same (i.e. none).

## Current approach

Build the site locally to the `docs` folder (as opposed to the default `_sites` folder) with the following:

```
npx @11ty/eleventy --input=. --output=docs
```

This is because GitHub Pages gives you the option to serve the site from either the `master` branch or the `master` branch `/docs` folder.

Put a `.nojekyll` file in the repo to stop GitHub Pages using Jekyll by default.

Set up GitHub Pages to serve the site from the `/docs` folder.

## Future approach

Stop doing all that crap above and use GitHub Actions to do it properly somehow.
