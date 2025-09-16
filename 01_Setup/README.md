# 01 Python & Pyenv Setup

   Note: This setup is for macOS, for Windows, please refer to the [Pyenv Windows documentation](https://github.com/pyenv-win/pyenv-win). 

There are two ways of executing Python code: Locally on your machine or in a cloud environment such as [Google Colab](https://colab.research.google.com/). For an optimal workflow and to avoid data protection issues a local working environment is encouraged. To setup Python on your local machine follow the steps below. 

   Note: For this setup you will work with your computers **command line interface** (CLI). On Mac this is the **[Terminal](https://support.apple.com/de-de/guide/terminal/trmld4c92d55/mac)** on Windows the **[Command Prompt](https://www.lifewire.com/how-to-open-command-prompt-2618089)**. If you want to learn more about your CLI and it's magnificent abilities for designers, check this [tutorial](https://ffd8.github.io/cli-for-artists-and-designers/) by Ted Davis (Mac/Terminal).

If you have a Mac, it is likely that you already have Python installed. You can check it by typing either `python --version` or `python3 --version` inside your terminal. If Python is installed, it will return a version number (e.g., `Python 3.9.7`). **However, you don't want to touch your so-called "system" Python to avoid problems and rather install our own version.**

Also, when working with Python, different projects may need different versions of Python. For example, one project might only run on Python 3.9, while another requires Python 3.12. Installing and switching between these versions manually can be messy.

[Pyenv](https://github.com/pyenv/pyenv) makes this easy:
- It lets you install multiple versions of Python side-by-side.
- You can quickly switch between them for different projects.
- It keeps your system Python (the one your Mac/Windows comes with) separate and safe.

The following documentation will walk you through all steps.

## 1. Installing Homebrew

Homebrew is a package manager for macOS — it works a bit like an “app store” for the terminal, letting you install and update software with simple commands instead of dragging apps around manually. Tools like pyenv aren’t regular apps with a clickable installer; they’re command-line utilities that need to be integrated into your shell (Terminal), so downloading a .dmg file like you would for Chrome or Zoom won’t work. On macOS, a package manager like Homebrew makes sense because it automatically puts these tools in the right place, keeps them updated, and handles all the little system details for you.

Go to the [Homebrew](https://brew.sh/de/) website and follow the installation instructions. 

Verify the installation by typing the following into your terminal: 

```sh
brew --version
```

## 2. Installing X-Code

Xcode provides the essential developer tools that let your computer compile and run code. Even if you’re not building iOS apps, many programming languages and libraries on macOS rely on these tools to work properly. Install it with the following command: 

```bash
xcode-select --install
```

You can check if it is installed with `xcode-select -p`

## 3. Installing Pyenv

Install Pyenv using Homebrew with:

```bash
brew install pyenv
```

You can verify the installation with `pyenv --version`. You should see a version number. 

## 4. Install Pyenv Dependencies

To use Pyenv and install Python versions, the [developers of Pyenv recommend](https://github.com/pyenv/pyenv/wiki#suggested-build-environment) to install certain dependencies with Homebrew too:

```zsh
brew install openssl readline sqlite3 xz tcl-tk@8 libb2 zstd zlib pkgconfig
```

## 5. Set up your shell environment for Pyenv

With Pyenv installed, you need to tell your shell to always listen to Pyenv instead of bypassing it and running your system Python. For this you need to add some code to your shell profile. First check which shell you use by typing `echo $SHELL` into your terminal. 

- If you see /bin/bash → you’re using Bash.
- If you see /bin/zsh → you’re using Zsh.

The shell profile file is a hidden file (file that starts with a `.`) in your root user folder. Usually you find it under `Macintosh HD > Users > your-user > .zshrc`. Press `COMMAND + SHIFT + .` to show/hide the hidden files. 

Zsh is the default shell of most modern macbooks, this means you should see a `.zprofile` and maybe a `.zshrc`.

In your terminal add the following code to create (or update) a `.zshrc` file: 

```zsh
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo '[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init - zsh)"' >> ~/.zshrc
```
**Now you should be ready with Pyenv!**

## 6. Install Python with Pyenv

You can see all possible Python versions to install with `pyenv install --list`

You can install a specific version with: 

```zsh
pyenv install 3.13.0
```

You can uninstall a specific version with: 

```zsh
pyenv uninstall 3.13.0
```

Now you can set the global Python version with:

```zsh
pyenv global 3.13.0
```

## 7. Verifying

1. To verify that everything worked type `pyenv versions`. You should see your installed Python version number and a * to show that its global. 
2. Type `which python` and verify that the path it outputs points towards pyenv, it should look something like `/Users/your-user/.pyenv/shims/python`

Now you are ready to go!! 🥷

## 8. Setting Up VS Code for Python and Jupyter Notebooks

### Installing Python Extensions

1. Click on the Extensions icon on the left sidebar (or press `Ctrl+Shift+X` / `Cmd+Shift+X` on Mac).
2. Search for **Python** and install the extension by Microsoft.
3. Search for **Jupyter** and install the extension by Microsoft.
4. Search for **Pylance** and install the extension by Microsoft (Auto-complete feature).

These extensions will automatically install a few other, thats fine and you don't need to worry about it. 

### Running Jupyter Notebooks in VS Code

1. Open the provided folder "python-introduction" in VS Code
2. Open the file `test.ipynb`.
3. On the top right corner of VS Code, click **"Select Kernel"** and choose the installed Python environment.
4. In the center top of VS Code click **"Run All"**.  You should see a `hello world!` message underneath the code cell. 

All done? Nice! 👍 You are on your way to become a master coder. 🥷