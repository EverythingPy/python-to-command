# python-to-command
How to make a Python script a command.

It is faster and more easy to run a command from any directory that having to <code>cd</code> until you find the binary and run it.
As commands come from executable files in the directory <code>/bin</code>, you can make a Python script a executable using PyInstaller.
Then you can move the binary file to <code>/bin</code> and therefore, run it from your terminal!

1. Make a virtual enviroment (or venv):
Make the venv:
```bash
python3 -m venv .
```
Note: This will create a venv in your current directory.\n
2. Activate the venv:
```bash
source bin/activate
```
3. Install PyInstaller using pip::
```bash
pip install pyinstaller
```
4. Make your Python script a executable using PyInstaller:
```bash
pyinstaller --onefile <your-script-name>.py
```
5. Change permissions:
```bash
chmod +x <your-executable-name>
```
6. Move to /bin:
```bash
sudo mv <your-executable-name> /bin
```
7. Run your script!
```bash
<your-executable-name>
```
