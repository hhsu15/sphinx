# sphinx

## Installation

```bash
pip install sphinx
```

## Get started

Run this script and it will create the files for you.

```bash
mkdir docs
cd docs
sphinx-quickstart
```

The `index.rst` is the main file for the home page as well as strcucture of your documentations.

Refer this chichi for rst (reStructuredText) or the actual example `first_page.rxt`

To build the html content, run:

```bash
# sphinx-build -b html <source_dir> <build_dir>, for example
sphinx-build -b html . _build
```

To change the theme, you have to install it mannually,

```bash
pip install sphinx_rtd_theme
```

then, in the `conf.py`:

```python
html_theme = "sphinx_rtd_theme"
```

## Host documentation on github page

After you push your docs dir to the repo, create a branch called `gh-pages`.

Then just copy everything in the `_build` folder into this branch' root directory,
once that's done,

1. Go to the github repo -> `settings` -> Github Pages
2. Select from the dropdown: main -> root # since we move everythin in the root
3. Save it and it will take a few minutes to deploy to url.

Refer to the Makefile for on-going auto-deplopy
