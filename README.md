# Python Biella Group: Bear

This project it's the base template for a Python project that we are using in PythonBiellaGroup to create our tools, libraries and projects.

We call it **Bear** because it's a **B**ase **E**nvironment for **A**ny **R**easonable project and also because the bear it's the symbol of the city of Biella.

It's based on **Modern Python Tools** such as:
- cookiecutter: for templating
- poetry: for dependency management
- pdm: for dependency management
- flake8: for linting
- mypy: for static type checking
- black: for code formatting
- bandit: for security checks
- pre-commit: for pre-commit hooks
- ruff: for linting

We suggest to use **VSCode** as IDE for this project since you can find a lot of prepared configurations for:
- debugging
- testing
- settings
- extensions

You can find and extensive documentation created with **mkdocs** to [this github page link](https://pythonbiellagroup.github.io/bear/)

## Next step

1. ~~Fix cookiecutter for windows powershell usage~~
2. Add mkdocs implementation on Base package with an example with python code
3. Publish mkdocs documentation page on gitlab pages
4. Add sphynx implementation with cookiecutter rule to choose between mkdocs and sphynx
5. ~~Fix pre-commit~~
6. Add better implementation of detect-secrets
7. Add a system to check dependencies updates, vulnerabilities and security issues
8. Better README documentation and CONTRIBUTING documentation
9. ~~Fix the docker with poetry~~
10. ~~Fix the devcontainer~~
11. ~~Add a docker container with PDM installation~~
12. Add gitlab pipeline example
13. Add github pipeline example
14. ~~Add package build~~


## How to use it

You can use this repository as a template to create your own project with **cookiecutter**

Just remember to add **cookiecutter** as a dependency into your local version installation of python using pip (or something else)
```bash
pip install cookiecutter
```

You can use this following command (both on Windows and Posix systems):
```bash
# If you are using https
cookiecutter https://github.com/PythonBiellaGroup/Bear.git

# If you are using ssh
cookiecutter git@github.com:PythonBiellaGroup/Bear.git
```

once you launch this commands just follow the guide and fill the required fields.

You can also create an Alias for this command to make it easier to use it in your terminal:
```bash
# If you are using https
alias pbg-project="cookiecutter https://github.com/PythonBiellaGroup/Bear.git --overwrite-if-exists"

# If you are using ssh
alias pbg-project="cookiecutter git@github.com:PythonBiellaGroup/Bear.git --overwrite-if-exists"
```

so you can use simply the command: `pbg-project` after you restart your terminal to download and create a new project.

## How to maintain it

Unfortunately there is no automatic way to update the templates inside cookiecutter yet, you have to do it manually.

1. Clone the repository
2. Launch the dependency installation using: poetry or pdm
   1. `poetry install`
   2. or `pdm install`
3. Modify something
4. If you want to test a specific inner template (like the Base template) you can launch: `cookiecutter .` to test cookiecutter project generation
   1. After that you can modify the template
   2. When you finish your modification you have to copy and paste all the modifications manually inside the cookiecutter generation folder
5. Then remember to open a pull request or push to the repository (in develop firtst) if you have the permissions.

Please remember also to follow a Gitflow workflow and to use the **develop** branch as the main branch for development.

### Technical Documentation

We use **mkdocs** to create the documentation for this project.

To launch the documentation locally:(remember to install the python env with poetry or pdm before):
```bash
mkdocs serve
```

If you want to prepare the build artifacts for the **gitlab pages** documentation, you have to run:
```bash
mkdocs build
```

## How to contribute

You can help us to improve this project by opening issues or doing some pull request if you want to add more functionalities or if you want to fix some bugs.

Please follow the [Contributing guidelines](CONTRIBUTING.md) to contribute to this project.

## License

This repository is licensed under the MIT license. See LICENSE file for details.

If you use this repository in your work, please cite it as or just write to us to say thanks with your feedback and experience :)

## Known issues

With mac if you want to use `devcontainer` with vscode probably you will experience a long building time on the first time. This is due to the `amd64` base docker image we are using as a baseline.

## References

Useful links and other documentation website you can check

- [Our website with the documentation](https://pythonbiellagroup.it)
- [The repository for our documentation](https://github.com/PythonBiellaGroup/doc-website)
- [Hypermodern python repository](https://github.com/cjolowicz/hypermodern-python)
- [The hypermodern python official medium article](https://medium.com/@cjolowicz/hypermodern-python-d44485d9d769)
- [Modern Python repository](https://github.com/rhettinger/modernpython)
- [Awesome Pyproject](https://github.com/carlosperate/awesome-pyproject/blob/master/README.md)
- [Python developer roadmap](https://roadmap.sh/python/)
- [Creating a modern python development environment medium article](https://itnext.io/creating-a-modern-python-development-environment-3d383c944877)
- [Modern python interesting practices](https://www.stuartellis.name/articles/python-modern-practices/)
- [4 Keys to write modern python in 2022](https://www.infoworld.com/article/3648061/4-keys-to-writing-modern-python-in-2022.html)
- [cookiecutter-poetry good implementation](https://github.com/fpgmaas/cookiecutter-poetry)
- [dev container video tutorial](https://www.youtube.com/watch?v=0H2miBK_gAk)
- [Ruff official documentation](https://github.com/charliermarsh/ruff/blob/main/README.md)
- [Ruff vscode extension](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff)
