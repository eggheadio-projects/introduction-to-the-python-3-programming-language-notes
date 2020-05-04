# [Manage packages with pip in Python](https://egghead.io/lessons/python-manage-packages-with-pip-in-python)

## Installing Packages with `pip`

`pip` is like npm for JavaScript. It is should be installed by default. It's also installed when you use a virtual environment.

To install a package, just type `pip install` followed by the package name you want in your virtual environment.

Once a package is installed, we can import it to the Python file we'd like to use it in.

## Figuring Out What Packages You Need

You won't always know the specific name of the package you want to use. In those times, it's good to use Google. Make sure to include the purpose of the package you need along with Python in your Google search.

### `pip search`

If you don't know the name of the package you're interested in, you can also use `pip search`. This isn't as efficient though because there can be lots of results.

```bash
pip search aws
```

## `pip list`

Using  `pip list` will show you all the packages that have been installed in your Python environment.

### `pip list --outdated`

This command will list all the packages that are not up to date or at the latest stable version.

## `pip uninstall`

You can uninstall a package using `pip uninstall` followed by the name of the package you want to get rid of.

Check notes on [02.md](02.md) for more info on virtual environments.