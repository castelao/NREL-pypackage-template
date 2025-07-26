# Template for NREL's Python packages

This is an opinionated template for creating Python packages at NREL
intended for a wide range of users. If you are new to NREL or don't have
much experience building Python packages, this template is a good option
to provide you a scaffolding to get started quickly. It also setup several
support tools such checks on your code, documentation generation, and
running tests.
If you're an experienced Python developer, you still have some control by
answering a few questions during the initialization process, while avoiding
a plain copy and paste from some of your other projects. We use this
template ourselves.

## Quickstart

### Install Copier

This template is based on [Copier](https://copier.readthedocs.io), a tool to
copy files and directories from a template repository to a destination
directory, while allowing you to answer questions to customize the
destination. You can install `copier` in several ways, depending on your
environment and preferences. Here are some common methods, please choose one
that suits you best:


#### Homebrew (OSX)

If you are on OSX and have [Homebrew](https://brew.sh/), you can install
`copier` globally with the following command:

```bash
brew install copier
```

#### Pixi (contributors)

If you have [Pixi](https://pixi.sh/latest/) installed, you can:

- Clone this repository and activate it's environment:
  ```bash
  git clone https://github.com/castelao/NREL-pypackage-template
  cd NREL-pypackage-template
  pixi shell
  ```
- Or create your own environment:
  ```bash
  pixi init my_project_creator
  pixi add copier
  pixi shell
  ```

We use pixi for development. If you would like to contribute to this repository or want to build your own template, we strongly recommend using Pixi.

#### uv

If you prefer using [uv](https://docs.astral.sh/uv/#tool-management), you can install `copier` with the following command:

```bash
uv tool install copier
```

Note: If you use `poetry`, you might want to consider moving to `uv`.

#### pipx

If you have [pipx](https://pypa.github.io/pipx/) installed, you can install `copier` with the following command:

```bash
pipx install copier
```

#### Nix flake

If you are using [Nix flakes](https://nixos.wiki/wiki/Flakes), you can install `copier` with the following command:

```bash
nix profile install 'https://flakehub.com/f/copier-org/copier/*.tar.gz'
```




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
