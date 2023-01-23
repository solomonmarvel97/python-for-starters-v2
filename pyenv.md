# Pyenv

## Using multiple python versions using pyenv

`pyenv` is a tool that allows you to easily install and switch between multiple versions of Python on a single machine. It is particularly useful if you need to work with multiple projects that require different versions of Python, as it allows you to switch between the different versions without affecting the global Python installation on your system.

To install `pyenv`, you will first need to ensure that you have the necessary dependencies installed on your system.

On Linux and Mac devices use the command below:

```bash
curl https://pyenv.run | bash
```

On a Debian or Ubuntu system, you can install the dependencies with the following command:

```bash
sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev
```

To install `pyenv` on a Windows machine, installing with PowerShell is the easiest way to get started. Open PowerShell and run the command below:

```powershell
Invoke-WebRequest -UseBasicParsing -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "./install-pyenv-win.ps1"; &"./install-pyenv-win.ps1"
```

If you encounter any error during installation on Windows, use the link below to find possible solutions: [https://github.com/pyenv-win/pyenv-win/blob/master/docs/installation.md#powershell](https://github.com/pyenv-win/pyenv-win/blob/master/docs/installation.md#powershell)

Once the dependencies are installed, you can install `pyenv` with the following command:

```bash
curl https://pyenv.run | bash
```

This will install `pyenv` and add the necessary configuration to your shell. To start using `pyenv`, you will need to add the following lines to your shell configuration file (e.g. \~/.bashrc, \~/.zshrc, etc.):

```bash
export PATH="~/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

After adding these lines, you can either log out and log back in again or source your shell configuration file to apply the changes:

```bash
source ~/.bashrc
```

With `pyenv` installed, you can now use the `pyenv` command to list the available Python versions, install new versions, and switch between them. For example, to list the available Python versions, you can use the `pyenv install --list` command.

To install a specific version of Python, you can use the `pyenv` install command followed by the version number. For example, to install Python 3.9.0, you can use the following command:

```bash
pyenv install 3.9.0
```

Once you have installed multiple versions of Python using `pyenv`, you can switch between them using the `pyenv` global command. For example, to switch to Python 3.9.0, you can use the following command:

```bash
pyenv global 3.9.0
```

This will set the global Python version to 3.9.0, and any new Python environments or virtual environments that you create will use this version by default. You can also set the Python version on a per-project basis by creating a `.python-version` file in the root directory of your project, and specifying the desired Python version in the file. `pyenv` will automatically switch to the specified version whenever you enter the project directory.
