# {{ cookiecutter.project_name }}

Built using `cookiecutter`

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

## `poetry` + `pyenv` usage

### Set local `pyenv` environment

Let's say you want to create an environment using python version {{ cookiecutter.python_version }} (default: 3.10.6)

```bash
pyenv install {{ cookiecutter.python_version }}
```
Then navigate to the root directory and make it your local version:

```bash
pyenv local {{ cookiecutter.python_version }}
```

This creates a `.python-version` file. During cookie creation this should have prompted you for this for convenience

### Install dependencies and create the virtual env in `poetry`

```bash
# Install required libraries
poetry install
```

This will install the dependencies and the {{ cookiecutter.package_name }} package and create a virtual environment and virtual shell. You can exit the virtual shell with crtl+d or `exit` in terminal.

### Resuming work

Next time you enter into the directory, `pyenv` will detect and activate local python version and then you can restart the shell:

```bash
poetry shell
```
## Testing

Run all tests in the `tests\` folder:

```bash
poetry run pytest
```

## Git

See this [gist](https://gist.github.com/mindplace/b4b094157d7a3be6afd2c96370d39fad) for a reminder on the steps to initialize this as a git repo and push to a remote, empty repo.