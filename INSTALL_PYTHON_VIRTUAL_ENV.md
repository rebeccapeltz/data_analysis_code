# Installing Python and Setting up a Virtual Environment

## Python Installation Options

- Mac or Windows users can download open source Python for free from
python.org.  
- Mac users can also use Homebrew to install Python.  
- Linux users can use the package managers like apt (Ubuntu, Debian), dnf
(Fedora), or yum (CentOS).  
- Anaconda is a free open source data science platform that is available to
Windows, Mac and Linux platforms.  
If you are new to Python and using Windows or a Mac, you might want to start with
python.org as there is help and a community available.

## Python Virtual Environment

A Python virtual environment is useful for creating a project that depends on installed packages. Packages give Python access to code functionality beyond the basic language.  
If you do not use a virtual environment and install a Python package globally, you may run into problems when different projects require different versions of a package. The virtual environment allows you to select the versions that you need for the project you’re working on.  

With a virtual environment in place you can rely on **Isolation** , **Cleanliness** and **Reproducibility**.  
- **Isolation:** Prevents conflicts between dependencies of different projects. Project A might need libraryX version 1.0, while Project B needs libraryX version
2.0. With virtual environments, each project can have its specific dependencies
without clashing.
- **Cleanliness**: Keep your global Python installation clean and free from
project-specific clutter.
- **Reproducibility**: Makes it easier to share your project with others. You can provide a requirements.txt file (generated with `pip freeze requirements.txt`) that lists all project dependencies, allowing others to
easily recreate your environment.

## Anaconda

The Python Anaconda installation provides a virtual environment. If you are using a
[python.org](https://www.python.org/) or [Homebrew](https://docs.brew.sh/Homebrew-and-Python) install, you will need to set up your own virtual environments.
A virtual environment is associated with a directory on your file system.
If you are using Anaconda already, you can continue to use it for this course.

## Setting Up Virtual Environments

If you're using Python downloaded directly from python.org (or installed via a
package manager like apt on Linux, brew on macOS, or a standard Windows installer,
as opposed to Anaconda), the standard and recommended way to create a virtual
environment is using the built-in venv module.
Here are the instructions:

## Creating a Virtual Environment with venv
The venv module is included with Python 3.3 and later, so you don't need to install
anything extra.

### Mac or Linux 

Note: These instructions assume you can use Bash or Zsh commands. If you are using a Mac, you likely use Zsh which uses the same commands as Bash. 
 
**Step 1: Open Terminal**  
- **macOS / Linux:** Open your "Terminal" application.  

**Step 2: Navigate to Your Project Directory (Optional but Recommended)**  
It's good practice to **create your virtual environment inside your project's main
directory**. If you don't have one yet, you can create one.  

```bash
# Create a new directory for your project
mkdir my_python_project 

# Change into that directory 
cd my_python_project
```

If you already have a project directory, navigate into it:  

```bash
# change directory to an existing directory
cd path/to/your/existing_project
```

**Step 3: Create the Virtual Environment**  
Once you are in your desired directory, run the following command to create a virtual environment. You can name the environment anything you like, but common
conventions are `venv`, `.venv`, or `env`.  

```bash
python3 -m venv venv
```

- `python3`: This invokes your Python interpreter. 
- `-m venv`: This tells Python to run the venv module as a script.   
- `venv`: This is the name of the directory where your virtual environment will be
created. You can replace venv with any name you prefer (e.g., `myenv`, `env`,
`.venv`). 

This command will create a new directory (e.g., `venv`) in your current location. Inside this directory, you'll find a copy of the Python interpreter, pip, and other necessary files for an isolated environment.  

**Step 4: Activate and Verify the Creation of Virtual Environment**  
After creation, you need to "activate" the virtual environment. Activating it modifies your terminal's PATH variable for that session so that python, pip, and jupyter (if installed in the venv) refer to the executables within the virtual environment, not your global Python installation.  

```bash
source venv/bin/activate
```
After you activate the virutal envornment, your project directory should be preceded by the
name you gave the virtual environment.  For example, if you create a virtual environment in 
`path/to/your/existing_project`, and you used `venv` for your virtual envornment, you'll see the prompt is prefaced by `(venv)`:   
`(venv) path/to/your/existing_project`.  
This verifies the creation of the virutal environment.  



### Windows
**Step 1: Open Command Prompt**  
- **Windows:** Search for "cmd" or "Command Prompt" in the Start Menu and open it.
Check that python is installed and accessible from the Windows shell.

```shell
where python
```
**Step 2: Navigate to Your Project Directory (Optional but Recommended)**  

```shell
cd path\to\your\existing_project
```

**Step 3: Create the Virtual Environment**  
Once you are in your desired directory, run the following command to create a virtual environment. You can name the environment anything you like, but common
conventions are `venv`, `.venv`, or `env`.  

```shell
python -m venv venv
```

**Step 4: Activate and Verify the Creation of Virtual Environment**  

```shell
.\venv\Scripts\activate
```
After you activate the virutal envornment, your project directory should be preceded by the
name you gave the virtual environment.  For example, if you create a virtual environment in 
`path\to\your\existing_project`, and you used `venv` for your virtual envornment, you'll see the prompt is prefaced by `(venv)`:

```shell
(venv) path\to\your\existing_project
```

This verifies the creation of the virutal environment.

### Using 'pip' to Install Modules on Mac, Linux and Windows

Once you have installed a virtual environment, you can use the `pip` package installer to
install modules locally.  Verify that you have successfully installed a virtual environment 
by checking for pip.

```
pip --version
```

**Install Packages within the Virtual Environment**  

Now that your virtual environment is active, you can install any Python packages you need for your project using **pip**. These packages will be installed **only** within this virtual environment and will not affect your global Python installation or other virtual environments.  

```bash
pip install jupyter pandas
```

**Launch Jupyter Notebook**  

If you installed jupyter within your active virtual environment you can launch a web page that allows you to create and use [Juypter Notebook](https://docs.jupyter.org/en/latest/). 

```bash
jupyter notebook
```

This will launch Jupyter Notebook using the Python and packages from your activated
venv.  

## Deactivating the Virtual Environment on Mac, Linux or windows
When you're done working on your project or want to switch to another environment,
simply type:

### Mac or Linux
```bash or shell
source deactivate
```


Your terminal prompt will return to normal, and python, pip, etc., will once again refer to your global Python installation.


