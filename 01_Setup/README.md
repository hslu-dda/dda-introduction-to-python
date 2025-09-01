# 01 Setup

There are two ways of executing Python code: Locally on your machine or in a cloud environment such as [Google Colab](https://colab.research.google.com/). For an optimal workflow and to avoid data protection issues a local working environment is encouraged. To setup Python on your local machine follow the steps below. 

# Local Python Setup

Note: For this setup you will work with your computers **command line interface** (CLI). On Mac this is the **[Terminal](https://support.apple.com/de-de/guide/terminal/trmld4c92d55/mac)** on Windows the **[Command Prompt](https://www.lifewire.com/how-to-open-command-prompt-2618089)**. If you want to learn more about your CLI and it's magnificent abilities for designers, check this [tutorial](https://ffd8.github.io/cli-for-artists-and-designers/) by Ted Davis (Mac/Terminal).

## 1. Checking if Python is already Installed

Before installing Python, check if it is already available on your system.

### Mac

Open the Terminal and run:

```sh
python3 --version
```
and/or:
```sh
python --version
```
If Python is installed, it will display a version number (e.g., `Python 3.9.7`). Proceed with step 3.

Note: It is possible to have multiple different Python versions installed on your computer. On a Mac you might see both `python` and `python3` because older Macs came with an older version of Python called Python 2 (run with python), and when you install the newer Python 3 it gets its own command (python3) so the computer can tell them apart.

### Windows

Open Command Prompt (Win + R, then type `cmd` and press Enter) and run:
```sh
python --version
```
Or:
```sh
py --version
```
If Python is installed, it will display a version number (e.g., `Python 3.9.7`). Proceed with step 3.

---

## 2. Installing Python (If Not Installed)

If Python is not installed, follow the instructions below:

### Mac

1. Download the latest Python version from the official website: [https://www.python.org/downloads/macos/](https://www.python.org/downloads/macos/)
2. Run the installer and follow the instructions.
3. Verify the installation with terminal by typing:

```sh
python3 --version
```
Or
```sh
python --version
```

### Windows

1. Download Python from the official website: [https://www.python.org/downloads/windows/](https://www.python.org/downloads/windows/)
2. Run the installer. If asked check the box **"Add Python to PATH"**.
3. Click **Install Now** and follow the prompts.
4. Verify the installation:
   ```sh
   python --version
   ```
   Or:
   ```sh
   py --version
   ```

---

## 3. Verifying and Installing pip on Mac and Windows

After installing Python, check if pip (Python's package manager) is installed. Pip is used to add new libraries to your Python environment. 

```sh
pip --version
```
Or, if using Windows:
```sh
py -m pip --version
```

If pip is not installed, install it: 

### Install pip on Mac/Linux

```sh
python -m ensurepip --default-pip
python -m pip install --upgrade pip
```

Verify that the installation was successfull with `pip --version`.

### Install pip on Windows

```sh
py -m ensurepip --default-pip
py -m pip install --upgrade pip
```

Verify that the installation was successfull with `pip --version`.

---

## 4. Installing Pyenv & Homebrew

When you work with Python, different projects may need different versions of Python.  
For example, one project might only run on **Python 3.9**, while another requires **Python 3.12**.  
Installing and switching between these versions manually can be messy.  

[pyenv](https://github.com/pyenv/pyenv) makes this easy:
- It lets you install multiple versions of Python side-by-side.
- You can quickly switch between them for different projects.
- It keeps your system Python (the one your Mac/Windows comes with) separate and safe.

### Mac

To install Pyenv you need [Homebrew](https://brew.sh/de/). Homebrew is a package manager for macOS — it works a bit like an “app store” for the terminal, letting you install and update software with simple commands instead of dragging apps around manually. Tools like pyenv aren’t regular apps with a clickable installer; they’re command-line utilities that need to be integrated into your shell (Terminal), so downloading a .dmg file like you would for Chrome or Zoom won’t work. On macOS, a package manager like Homebrew makes sense because it automatically puts these tools in the right place, keeps them updated, and handles all the little system details for you.

Go to the [Homebrew](https://brew.sh/de/) website and follow the installation instructions. Verify the installation by typing the following into your terminal: 

```sh
brew --version
```
Your good to go if you see a version number like `Homebrew 4.5.8`. Proceed by installing [pyenv](https://github.com/pyenv/pyenv) using Homebrew, type the following command:

```sh
brew install pyenv
```

You can verify the installation by typing: 

```sh
# outputs something like 'pyenv 2.6.3'
pyenv --version
```

### Windows

To install Pyenv on Windows please follow the steps on the official [Github page](https://github.com/pyenv-win/pyenv-win). 

## 5. Setting Up VS Code for Python and Jupyter Notebooks

### Installing Python Extensions

1. Click on the Extensions icon on the left sidebar (or press `Ctrl+Shift+X` / `Cmd+Shift+X` on Mac).
2. Search for **Python** and install the extension by Microsoft.
3. Search for **Jupyter** and install the extension by Microsoft.

These extensions will automatically install a few other, thats fine and you don't need to worry about it. 

### Running Jupyter Notebooks in VS Code

1. Open the provided folder "python-introduction" in VS Code
2. Open the file `test.ipynb`.
3. On the top right corner of VS Code, click **"Select Kernel"** and choose the installed Python environment.
4. In the center top of VS Code click **"Run All"**.  You should see a `hello world!` message underneath the code cell. 

All done? Nice! 👍 You are on your way to become a master coder. 🥷