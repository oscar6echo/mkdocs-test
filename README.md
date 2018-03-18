## MkDocs Test

## 1 - Build conda environment

From terminal:

```bash
$ conda create -n docs python=3
$ source activate docs
$ pip install mkdocs
$ pip install mkdocs-material
$ conda env export > env_docs.yml
$ source deactivate
```

References:
+ [mkdocs](http://www.mkdocs.org/) documentation
+ [mkdocs-material](https://squidfunk.github.io/mkdocs-material/) documentation
+ [pymdown-extensions](https://facelessuser.github.io/pymdown-extensions/) documentation

## 2 - Serve docs in development mode

From terminal:

```bash
$ activate docs
# this serve current docs/ folder on localhost:8000 with hot reload
(docs) $ mkdocs serve
```

## 3 - Build docs

From terminal:

```bash
# this creates / overwrites folder site
(docs) $ mkdocs build
```

## 4 - Deploy on gh-pages

From terminal:

```bash
$ git subtree push --prefix site/ origin gh-pages
```

Resulting docs available on [https://oscar6echo.github.io/mkdocs-test/](https://oscar6echo.github.io/mkdocs-test/)
