# Virtualenv

`virtualenv` is a tool used to isolate specific Python environments on a single machine, allowing you to work with multiple versions of Python packages and libraries without conflicts. This can be useful if you need to work on multiple projects that require different versions of packages, or if you want to test your code on multiple versions of Python.

Here's how you can use `virtualenv`:

* Install `virtualenv`:

```bash
pip install virtualenv
```

* Create a new virtual environment:

```bash
virtualenv myenv
```

This will create a new directory called "myenv" that contains a copy of the Python interpreter and libraries, as well as a script called activate that you can use to activate the environment.

* Activate the virtual environment:

```bash
source myenv/bin/activate
```

This will modify your shell prompt to indicate that you are now working in the virtual environment. Your virtual environment will also be the default Python interpreter until you deactivate it.

* Install packages: With the virtual environment active, you can now install packages using pip as you normally would. These packages will be installed in the virtual environment, rather than globally on your system.

```bash
pip install <package-name>
```

* Deactivate the virtual environment: When you are finished working in the virtual environment, you can deactivate it by running the following command:

```bash
deactivate
```

This will restore the original Python interpreter and libraries, and remove the virtual environment from your shell prompt.
