# Setting Up Python on Mac and Windows

## 1. Checking if Python is Installed

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
If Python is installed, it will display a version number (e.g., `Python 3.9.7`).

### Windows
Open Command Prompt (Win + R, then type `cmd` and press Enter) and run:
```sh
python --version
```
Or:
```sh
py --version
```
If Python is installed, it will display a version number.

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

## 3. Setting Up VS Code for Python and Jupyter Notebooks

### Installing Python Extensions
1. Click on the Extensions icon on the left sidebar (or press `Ctrl+Shift+X` / `Cmd+Shift+X` on Mac).
2. Search for **Python** and install the extension by Microsoft.
3. Search for **Jupyter** and install the extension by Microsoft.

### Running Jupyter Notebooks in VS Code
1. Create a file with the ending `.ipynb`.
2. Click **"Select Kernel"** and choose the installed Python environment.
3. Run cells by clicking the **Run** button.

Your Python and Jupyter setup in VS Code is now complete!

