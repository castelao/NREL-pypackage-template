# NREL's template for Python packages

## Quickstart

- Install [pixi](https://pixi.sh/latest/#installation)
- Create an environment with pixi to initiate new packages.
  For instance, I use
  ```bash
  mkdir -p ~/work/projects/control-center
  cd ~/work/projects/control-center
  pixi init -c conda-forge -v .
  ```
- Install copier
  ```bash
  pixi add copier
  ```
- Now you're ready to create a brand new Python package.
  ```bash
  pixi run copier copy https://github.com/castelao/NREL-pypackage-template ../my_new_project
  cd ../my_new_project
  ```

- Add your dependencies. Let's assume you depend on `xarray`:
  ```bash
  cd ~/projects
  pixi add xarray
  ```
