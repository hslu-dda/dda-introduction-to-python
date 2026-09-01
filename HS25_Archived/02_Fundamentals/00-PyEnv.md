# PyEnv

When you start working with Python, you’ll quickly notice that different projects often need different Python versions. For example, one project may run on Python 3.10, while another may require Python 3.12.
This is where pyenv helps: it lets you easily install, switch, and manage multiple Python versions on your computer.

## 1. Verify the Installation

```bash
pyenv --version
```

If the `pyenv` command isnt't recognized in your terminal, see here: [B. Set up your shell environment for Pyenv](https://github.com/pyenv/pyenv?tab=readme-ov-file#b-set-up-your-shell-environment-for-pyenv)


## 2. List all Python environments

```bash
pyenv versions
```

- system → the default Python that comes with your OS
- * → marks the currently active version

## 3. Install a specific Python version

**Important: Before installing Python versions its recommended to [install certain dependencies](https://github.com/pyenv/pyenv/wiki#suggested-build-environment):**

```bash
brew install openssl readline sqlite3 xz tcl-tk@8 libb2 zstd zlib pkgconfig
```

You can see all available versions with:

```bash
pyenv install --list
```

You can install a specific version with: 

```bash
pyenv install 3.11.5
```

You can uninstall a specific version with: 

```bash
pyenv uninstall 3.7.0
```

## 4. Creating and managing environments

pyenv lets you set Python versions in two main ways:

### Global

Sets the default version for your whole system (all projects):

```bash
pyenv global 3.11.5
```

### Local 

Sets the Python version for just one project folder. Inside the project directory:

```bash
pyenv local 3.11.5
```

This creates a hidden .python-version file in that folder.
When you’re inside that folder, pyenv will use the specified version.
Tip: Local settings override global ones.

Important: this only picks which Python interpreter you’re using (e.g. Python 3.12 vs 3.11).
It does not isolate your packages (e.g. Pandas). If you install a library with pip install, it goes into the global site-packages for that version.


### Virtual Environment

A virtual environment is a fully isolated Python installation that has its own site-packages.
This means different projects can have the same Python version, but with completely different installed libraries.

Create an virtual environment with: 

```bash
pyenv virtualenv 3.11.5 myproject-env
```

Activate it with: 

```bash
pyenv activate myproject-env
```

Inside this environment, `pip install pandas` won’t affect any other project — just this environment.

Deactivate it: 

```bash
pyenv deactivate
```

## 5. Further Ressources

- [Official Documentation](https://github.com/pyenv/pyenv)
- [Youtube Tutorial](https://www.youtube.com/watch?v=MVyb-nI4KyI&t=76s)
