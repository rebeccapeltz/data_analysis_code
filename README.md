# Analyzing Data using Python, Jupyter Notebook, Plotly and GitHub

## Install Python and Virtual Environment

See these [instructions](./INSTALL_PYTHON_VIRTUAL_ENV.md) to install Python and set up Virtual environment.

## Summary of Install and Run Jupyter Notebook Locally  

These are bash/zsh commands.  If you are using Windows see the instruction above to use Bash command on Windows.

If you are not in the directory containing this README
```bash
cd <directory containing this README>
```

Execute commands to install a Python Virtual environment in the document linked to above.
Once the virtual environment is activated run `pip install <package>` to install packages 
that will be used in this repository: `jupyter`, `pandas`, and `plotly`.

**Mac** and **Linux** users, execute these commands in the command line interface:

```bash
python3 -m venv venv
source venv/bin/activate
pip install jupyter
pip install plotly
jupyter notebook
```

**Windows** users, execute these command in the Window shell

```shell
python -m venv venv
.\venv\Scripts\activate
pip install jupyter
pip install plotly
jupyter notebook
```

The `jupyter` p makes it possible to use Jupyter Notebook locally. 
The `pandas` package provides functions to manipulate data in Python code.
The `plotly` module will be used to create data visualations.

