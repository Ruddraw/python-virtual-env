# Guide to Using Python Virtual Environment with `pipenv` and Setting Up a Django Project

This guide explains how to use Python virtual environments and set up the Python path with `pipenv`. We will create a Django project as an example.

## Step 1: Installing `pipenv`

First, we need to install `pipenv`. Run the following command:

- **Windows:**
```ruby
pip install pipenv
```
- **Linux/Mac:**
```ruby
pip install pipenv
```

## Step 2: Check Python Installation

Before proceeding, ensure that Python is installed on your system. You can check this by running:

- **Windows:**
```ruby
python --version
```
- **Linux/Mac:**
```ruby
python3 --version
```
If Python is not installed, download and install the latest version from [Python's Official Website](https://www.python.org/downloads/)

- **Step 3: Create a Directory and Install Django**
Next, create a directory for your project and navigate to it. Then, install Django using `pipenv`:

- **Windows:**
```ruby
mkdir project_directory
cd project_directory
pipenv install django
```
- **Linux/Mac:**
```ruby
mkdir project_directory
cd project_directory
pipenv install django
```


What `pipenv` does here is create a virtual environment that includes the required Django files. You can check the environment by visiting the path mentioned in the output of the command.
`pipenv` also generates two important files in your project directory:
  - `Pipfile`: This file specifies the Python packages required for the project. It is used to track project dependencies.
  - `Pipfile.lock`: This file ensures that all team members or deployments use the exact same package versions, providing consistency and avoiding potential conflicts.

## Step 4: Activate the Virtual Environment
To activate the virtual environment, run the following command:

- **Windows:**
```ruby
pipenv shell
```
- **Linux/Mac:**
```ruby
pipenv shell
```
This opens a shell with the virtual environment active, where you can run commands isolated from your system-wide Python environment.

## Step 5: Create a Django Project
To create a Django project within this virtual environment, run the following command:

- **Windows:**
```ruby
django-admin startproject projectname .
```
- **Linux/Mac:**
```ruby
django-admin startproject projectname .
```
Replace `projectname` with the name of your project.

## Step 6: Using VS Code's Integrated Terminal
Now, to set up VS Code to use the virtual environment's Python interpreter:

  1. Open the project directory in VS Code.

  2. Under the View menu, choose the option called Command Palette (shortcut: `Shift + Command + P` on macOS or `Ctrl + Shift + P` on Windows).

  3. Search for Python: Select Interpreter.

  4. By default, VS Code uses the global Python interpreter, but we want to use the one from the virtual environment. To find the path to the virtual environment, run this command in the terminal:
     
- **Windows:**
```ruby
pipenv --venv
```
- **Linux/Mac:**
```ruby
pipenv --venv
```
  5. This command will give you the path to the virtual environment. Copy the file path.

  6. Go back to VS Code, select Enter interpreter path, and paste the path you copied. Append `/Scripts/python` for Windows or `/bin/python` for Linux/Mac at the end.

Now, if you open the integrated terminal in VS Code, you should see that it automatically activates the virtual environment for this project.

## Step 7: Deactivating the Virtual Environment
To deactivate the virtual environment, simply run:
- **Windows:**
```ruby
exit
```
- **Linux/Mac:**
```ruby
exit
```
This will return you to your system’s global environment.

## Activating and Deactivating the Virtual Environment for Future Work
For activation:
- **Windows:**
```ruby
pipenv shell
```
- **Linux/Mac:**
```ruby
pipenv shell
```
For deactivation: 
- **Windows:**
```ruby
exit
```
- **Linux/Mac:**
```ruby
exit
```
