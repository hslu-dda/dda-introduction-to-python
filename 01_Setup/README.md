# Setting Up Python

There are two ways of executing Python code: Locally on your machine or in a cloud environment such as [Google Colab](https://colab.research.google.com/). For an optimal workflow and to avoid data protection issues a local working environment is encouraged. To setup Python on your local machine follow the steps below. 

However, if you run into serious problems installing Python on your machine which you can't resolve, it's okay to follow the introduction course using Google Colab. In this case, make sure to sign up to Colab before class starts. All you need for this is a Google account (e.g. an @gmail address).

# Setup Python Locally

Note: For this setup you will work with your computers **command line interface** (CLI). On Mac this is the **[Terminal](https://support.apple.com/de-de/guide/terminal/trmld4c92d55/mac)** on Windows **[Command Prompt](https://www.lifewire.com/how-to-open-command-prompt-2618089)**. If you want to learn more about your CLI and it's magnificent abilities for designers, check this [tutorial](https://ffd8.github.io/cli-for-artists-and-designers/) by Ted Davis.

## 1. Checking if Python is already Installed

Before installing Python, check if it is already available on your system.

### Mac
Open the Terminal and run:
```sh
python3 --version
```
Or:
```sh
python --version
```
If Python is installed, it will display a version number (e.g., `Python 3.9.7`). Proceed with step 3.

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

If pip is not installed it: 

### Install pip on Mac/Linux

```sh
python -m ensurepip --default-pip
python -m pip install --upgrade pip
```

Verify again with `pip --version`.

### Install pip on Windows

```sh
py -m ensurepip --default-pip
py -m pip install --upgrade pip
```

Verify again with `pip --version`.

---

## 4. Verifying and Installing Pandas

To check if pandas is installed, use. A message will appear including a version number of Pandas. 

```sh
pip show pandas
```

If pandas is not installed, install it using:

```sh
pip install pandas
```

Verify the installation again.

---

## 5. Setting Up VS Code for Python and Jupyter Notebooks

### Installing Python Extensions

1. Click on the Extensions icon on the left sidebar (or press `Ctrl+Shift+X` / `Cmd+Shift+X` on Mac).
2. Search for **Python** and install the extension by Microsoft.
3. Search for **Jupyter** and install the extension by Microsoft.

These extensions will automatically install a few other, thats fine and you don't need to worry about it. 

### Running Jupyter Notebooks in VS Code

1. Create a file with the ending `.ipynb`.
2. Click **"Select Kernel"** and choose the installed Python environment.
3. Create a Python cell and add the following code: 
```sh
name = "Alice"
print(f"Hello, {name}!")
```
4. Run the cell by clicking the **Run** button.

You should now see `Hello, Alice!` be printed below the cell. 
Congratulations, your Python and Jupyter setup in VS Code is now complete!

