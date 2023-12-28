# Starting a Python Project

Welcome to the world of Python 🐍🐍🐍! This guide will walk you through the initial steps of setting up a Python project, explaining key concepts and tools like Conda, Jupyter Notebooks, and more.

## Table of Contents
1. [Setting Up Conda](#setting-up-conda)
2. [Activating Conda Environment](#activating-conda-environment)
3. [Using VS Code with Conda](#using-vs-code-with-conda)
4. [Installing Jupyter Notebook](#installing-jupyter-notebook)
5. [Understanding Jupyter Notebooks](#understanding-jupyter-notebooks)
6. [Conclusion](#conclusion)
7. [Additional Resources](#additional-resources)

## Setting Up Conda

[Conda](https://docs.conda.io/en/latest/) is an open-source package management and environment management system that runs on Windows, macOS, and Linux. It lets you easily create, manage, and switch between different project environments with different Python versions and package sets.

### Creating a New Conda Environment

To create a new environment, use:

```bash
conda create --name myenv python=3.8
```

Replace `myenv` with your desired environment name and `3.8` with your preferred Python version.

## Activating Conda Environment

After creating your environment, you need to activate it to use it.

### On the Terminal

Run the following command:

```bash
conda activate myenv
```

Replace `myenv` with your environment name.

### In VS Code

VS Code can automatically detect and offer to activate Conda environments. This is handy for integrating your environment directly with your IDE.

## Using VS Code with Conda

Visual Studio Code (VS Code) is a popular IDE for Python development. It can integrate with Conda environments seamlessly.

### Activating Environment in VS Code

When you open a project in VS Code, it may prompt you to activate the Conda environment. Alternatively, you can select the Python interpreter from the bottom-right corner, which corresponds to your Conda environment.

### Difference Between Terminal and VS Code Activation

- **Terminal Activation**: This is universal and works in all shell environments. You need to do this every time you open a new terminal.
- **VS Code Activation**: It's specific to your project in VS Code. It ensures that the correct environment is used for linting, debugging, and running code within the IDE.

### When to Use Which?

- **Use Terminal Activation** when running scripts or managing packages outside VS Code.
- **Use VS Code Activation** for development within the VS Code environment to ensure consistency.

## Installing Jupyter Notebook

Jupyter Notebooks are an interactive computational environment, in which you can combine code execution, rich text, mathematics, plots, and rich media.

To install Jupyter Notebook in your Conda environment:

```bash
conda install -c conda-forge notebook
```

## Understanding Jupyter Notebooks

Jupyter Notebooks differ from scripts in that they allow a more interactive development experience. They are ideal for data analysis, visualization, and exploratory programming.

### How is it Different from a Script?

- **Jupyter Notebook - .ipynb**: Interactive, supports inline comments and media, great for visualization and exploratory analysis.
- **Python Script - .py**: Linear execution of code, more suitable for final, production-ready projects. Allows import of functions into other scripts or notebooks.

## Installing Additional Python Packages

Expanding your Python project often requires the installation of additional packages. This section covers how to install these packages using both Jupyter Notebooks and the terminal.

### In Jupyter Notebooks

Jupyter Notebooks allow you to install packages directly within the notebook environment.

#### Using the `!` Command

To install a package in a Jupyter Notebook, you can use the `!` command followed by `pip` or `conda`. For example:

```python
!pip install numpy
```

or

```python
!conda install -c conda-forge numpy
```

This command is run as if it's in the terminal. It affects the current Jupyter kernel and the underlying environment.

### In the Terminal

Installing packages through the terminal is straightforward and affects the environment globally.

#### Using Conda

With Conda, you can install packages specifically for the activated environment. For instance:

```bash
conda install numpy
```

This installs the `numpy` package in the currently active Conda environment.

### When to Use Which?

- **Use Jupyter Notebooks** for quick, on-the-fly installations within a specific notebook. This method is useful for exploratory data analysis or when working on specific projects in a Jupyter environment.
- **Use the Terminal** for more permanent installations that you want available across multiple projects or notebooks. This method ensures that the package is available every time you activate the Conda environment.

### Understanding the Difference

- **Jupyter Notebook Installation**: Affects only the specific notebook's kernel/environment. Ideal for temporary or project-specific installations.
- **Terminal Installation**: Affects the entire Conda environment. Best for packages you'll use across multiple projects or notebooks.

## Finding Installation Commands for Python Packages

When you need to find installation commands for various Python packages, here are some reliable sources:

#### PyPI (Python Package Index)

- **Website**: [PyPI](https://pypi.org/)
- **Description**: Official repository for Python packages. Provides `pip install` commands.

#### Conda Package Index

- **Website**: [Conda Package Index](https://anaconda.org/anaconda/repo)
- **Description**: Repository for Conda-compatible packages. Includes Conda installation commands.

#### GitHub Repositories

- **Usage**: Check the `README.md` or the `requirements.txt` of a package's GitHub repository.
- **Description**: Many Python packages provide installation instructions in their GitHub repositories.



Remember, always verify the source and ensure the instructions are compatible with your Python version and operating system.


## Conclusion

Starting a Python project involves setting up a proper environment, understanding the tools at your disposal, and knowing how to integrate them for a seamless development experience. As you grow more comfortable with these tools, you'll find that they greatly enhance your productivity and the quality of your code.

## Additional Resources

- [Conda Documentation](https://docs.conda.io/en/latest/)
- [Python Beginner's Guide](https://www.python.org/about/gettingstarted/)
- [Jupyter Notebook Documentation](https://jupyter-notebook.readthedocs.io/en/stable/)
- [Visual Studio Code Python Documentation](https://code.visualstudio.com/docs/languages/python)
- [Khan Academy Python Course](https://www.khanacademy.org/computing/intro-to-python-fundamentals)


