# Pipenv

#### Setting up virtual environments using pipenv

`Pipenv` is a tool that aims to bring the best of all packaging worlds (bundler, composer, npm, cargo, yarn, etc.) to the Python world. It automatically manages project packages through the `Pipfile` file as you install or uninstall packages.

`Pipenv` is a tool that aims to simplify the process of managing package dependencies in a Python project. It does this by introducing a new file called the `Pipfile`, which contains all the package dependencies for your project. You can use the `pipenv` command to install packages, and it will automatically update the `Pipfile` and `Pipfile.lock` with the new package information. The `Pipfile.lock` file is used to ensure that the exact same packages are installed on every machine that runs `pipenv` install, which can be useful for reproducing environments and avoiding dependency conflicts.

`Pipenv` is designed to be easy to use, and it integrates with other tools such as `pyenv` to manage multiple Python versions and `pipx` to install and run Python packages in isolated environments.

## Installing `pipenv`

To install `pipenv`, you will need to have Python and pip, the Python package manager, installed on your system. If you do not have Python and `pip` already installed, you can install them by following the instructions for your operating system:

**Windows:**

Download the Python installer from the official Python website (https://www.python.org/downloads/) and run it to install Python on your system. Make sure to select the option to add Python to your system path during the installation.

Open a Command Prompt window and run the following command to install pip:

```bash
python -m pip install -U pip
```

**macOS:**

Python and `pip` are pre-installed on macOS. You can check if they are installed on your system by running the following commands in a terminal:

```bash
python --version
pip --version
```

**Linux:**

Python and pip are often pre-installed on Linux systems. You can check if they are installed on your system by running the following commands in a terminal:

```bash
python3 --version
pip3 --version
```

If Python and pip are not installed on your system, you can install them by running the following commands:

```bash
sudo apt-get update
sudo apt-get install python3
sudo apt-get install python3-pip
```

Once you have Python and pip installed, you can install `pipenv` by running the following command:

```bash
pip install --user pipenv
```

This will install `pipenv` in your user directory, so you will be able to use it without having to use sudo. If you want to install `pipenv` system-wide, you can run the following command instead:

```bash
sudo pip install pipenv
```

This will install `pipenv` globally, allowing it to be used by any user on the system.

You can verify that `pipenv` is installed correctly by running the following command:

```bash
pipenv --version
```

This should print the version number of `pipenv`, indicating that it is installed and working correctly.

### Creating a virtual environment using `pipenv`

Run the following command to create a new virtual environment:

```bash
pipenv --python <python_version>
```

Replace \<python\_version> with the version of Python that you want to use in the virtual environment.

For example, to create a virtual environment with Python 3.7, you would run:

```bash
pipenv --python 3.7
```

To activate the virtual environment, run the following command:

```bash
pipenv shell
```

You should now see the virtual environment's name in your terminal prompt, indicating that it is active.

To install packages in the virtual environment, you can use `pipenv` install command. For example, to install the requests package, you would run:

```bash
pipenv install requests
```

To deactivate the virtual environment, simply run the exit command i.e.

```bash
exit
```
