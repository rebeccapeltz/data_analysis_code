# Link Virtual Environment to VS Code

If you are using VS Code to write your script, you can link your virtual environment to VS Code so that you can test without creating a server locally.

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

