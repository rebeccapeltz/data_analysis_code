# Link Jupyter Notebook Files to Python to VS Code

If you are using the VS Code IDE to write the Python Script in your Jupyter Notebooks, can make the Jupyter Notebook files execute the code in the file by installing the `ipykernel`.  A kernel is a management system that connects the front end (Jupyter Notebook) to the backend (Python).

If you've already installed Jupyter, you only need to install `ipykernel` to be able to run the code in the IDE files.


## Steps to Setting Up 'ipykernel' in Virtual Environment

Start by activating your environment if it isn't already activated.

```bash
source venv/bin/activate
```

Install Juypter inside the environment.

```bash
pip install jupyter ipykernel
```

Register the environment as a Jupyter kernel. If you named your environment something besides 'venv', used
that name for the --name parameter.

```bash
python -m ipykernel install --user --name=venv

```

## Select Kernel in VS Code

Select the venv kernal in VS Code. See image below.

![Select Jupyter Kernel in VS Code](./images/choose_kernel_vscode.jpg)

## Verify

```bash
import sys
print(sys.executable)
```
