# python-to-command

How to make a Python script a command.

It is faster and easier to run a command from any directory than having to `cd` until you find the binary and run it.
As commands come from executable files in the `/bin` directory, you can make a Python script executable using PyInstaller.
Then you can move the binary file to `/bin` and therefore run it from your terminal!

## Steps

1. **Make a virtual environment (venv):**

   ```bash
   python3 -m venv .
   ```
   Note: This will create a venv in your current directory.

2. **Activate the venv:**

   ```bash
   source bin/activate
   ```

3. **Install PyInstaller using pip:**

   ```bash
   pip install pyinstaller
   ```

4. **Make your Python script executable using PyInstaller:**

   ```bash
   pyinstaller --onefile <your-script-name>.py
   ```

5. **Change permissions:**

   ```bash
   chmod +x dist/<your-script-name>
   ```
   *Note: The executable will be found inside the `dist/` directory.*

6. **Move to `/usr/local/bin`:**

   ```bash
   sudo mv dist/<your-script-name> /usr/local/bin/
   ```
   *Note: It is recommended to use `/usr/local/bin` instead of `/bin` on most Unix systems.*

7. **Run your script:**

   ```bash
   <your-script-name>
   ```

7. Run your script!
```bash
<your-executable-name>
```
