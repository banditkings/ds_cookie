# nt_cookiecutter

A data science cookie cutter for `poetry` and `pyenv` user, which includes:

1. `poetry`
2. a `src` folder where the main module for shared code should exist in `src/package_name`
3. pre-commit hooks:
   1. autopep8
   2. poetry export -> requirements.txt 
4. A local `.python-version` for `pyenv`
5. Folder structure similar to `kedro`

Documentation on cookiecutter
https://cookiecutter.readthedocs.io/en/stable/

To create a new project folder that follows this cookiecutter template run:  

`cookiecutter git@github.com:banditkings/ds_cookie.git`
