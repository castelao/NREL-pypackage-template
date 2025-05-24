# Template for NREL's Python packages

This is an opinionated template for creating Python packages at NREL.

## Quickstart

- If you don't already have it, install [pixi](https://pixi.sh/latest/#installation)
- Clone this repository
  ```bash
  git clone https://github.com/castelao/NREL-pypackage-template.git
  cd NREL-pypackage-template
  ```
- Create your new project by running
  ```bash
  pixi run copier copy https://github.com/castelao/NREL-pypackage-template ../my_new_project
  cd ../my_new_project
  ```
  You should see several files and directories created from the information
  that you gave. For instance, take a look at the `pyproject.toml` file.
- Your package will probably depend on other libraries. Let's assume that
  you'll use `xarray`, so you can run
  ```bash
  pixi add xarray
  ```
  Which will update the `pyproject.toml` and `pixi.lock` files with the new
  dependency.
