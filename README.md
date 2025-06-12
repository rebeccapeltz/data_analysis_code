# Analyzing Data using Python, Jupyter Notebook, Plotly and GitHub

## Install Python and Virtual Environment

See these [instructions](./INSTALL_PYTHON_VIRTUAL_ENV.md) to install Python and set up Virtual environment.

## Summary of Install and Run Jupyter Notebook Locally  

These are bash/zsh commands.  If you are using Windows see the instruction above to use Bash command on Windows.

If you are not in the directory containing this README
```bash
cd <directory containing this README>
```

Execute command to install virtual environment and use local `pip` to install
jupyter and plotly.  Finally open Jupyter Notebook locally.

```bash
python3 -m venv venv
source venv/bin/activate
pip install jupyter
pip install plotly
jupyter notebook
```
The `jupyter` module makes it possible to use Jupyter Notebook locally.  The `plotly` module will be used for create graphs. 

