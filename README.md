# ds_cookie

A data science [cookiecutter](https://cookiecutter.readthedocs.io/en/stable/) for `poetry` and `pyenv` user, which includes:

1. `poetry`
2. a `src` folder where the main module for shared code should exist in `src/package_name`
3. pre-commit hooks:
   1. autopep8
   2. poetry export -> requirements.txt 
4. A local `.python-version` for `pyenv`
5. Folder structure similar to `kedro`

## Usage

To create a new project folder that follows this cookiecutter template run:  

```
python -m cookiecutter git@github.com:banditkings/ds_cookie.git
```

or if using HTTPS auth:

```
python -m cookiecutter https://github.com/banditkings/ds_cookie.git
```

## Project Structure

```
.
├── README.md                               <- The top-level README for developers using this project
│
├── data                                    <- Store raw data, features, etc - not committed to git
│
├── notebooks                               <- Jupyter notebooks. Naming convention is a number (for ordering),
│                                              the creator's initials, and a short `-` delimited description, e.g.
│                                              `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml                          <- Poetry dependency and environment file
│
├── reports                                 <- Generated analysis as HTML, PDF, LaTeX, etc
│   └── figures                             <- Generated graphics and figures to be used in reporting
│   
└── src                                     <- Source code for this project
    ├── tests                               <- All tests for this package
    └── {{ cookiecutter.package_name }}     <- This package
        ├── data                            <- Scripts to download or generate data
        ├── features                        <- Scripts to turn raw data into features for modeling
        ├── models                          <- Scripts to train models and then use trained models to make
        │                                      predictions
        └── visualization                   <- Scripts to create exploratory and results oriented visualizations
```

## Other project templates

* [Cookiecutter Data Science](https://drivendata.github.io/cookiecutter-data-science/)
* [Kedro Starters](https://github.com/kedro-org/kedro-starters)