# Contextualise Documentation

This repository contains the source files of [Contextualise](https://contextualise.dev/)'s documentation, in reStructuredText markup language (reST). They are meant to be parsed with the Sphinx documentation builder to build the HTML documentation.

## Contributing changes

**Pull Requests should use the `master` branch by default.**

Though arguably less convenient to edit than a wiki, this Git repository is meant to receive pull requests to always improve the documentation, add new pages and so forth. Having direct access to the source files in a revision control system is a big plus to ensure the quality of the documentation.

### Editing existing pages

To edit an existing page, locate its .rst source file and open it in your favorite text editor. You can then commit the changes, push them to your fork and make a pull request.

### Adding new pages

To add a new page, create a .rst file with a meaningful name in the section you want to add a file to, for example, `tutorials/associations/creating_generic_associations.rst`. Write its content like you would do for any other file, and make sure to define a reference name for Sphinx at the beginning of the file (check other files for the syntax). You should then add your page to the relevant "toctree" (table of contents, for example, `tutorials/associations/index.rst`). Add your new filename to the list on a new line, using a relative path and no extension.

### Sphinx and reStructuredText syntax

Check Sphinx's [reST Primer](https://www.sphinx-doc.org/en/stable/rest.html) and the [official reference](http://docutils.sourceforge.net/rst.html) for details on the syntax.

Sphinx uses specific reST comments to do specific operations, like defining the table of contents (`:toctree:`) or cross-referencing pages. Check the [official Sphinx documentation](https://www.sphinx-doc.org/en/stable/index.html) for more details, or see how things are done in existing pages and adapt it to your needs.

### Adding images and attachments

To add images, please put them in an `images/` folder next to the .rst file with a meaningful name and include them in your page with:

```rst
.. image:: images/image_name.png
```

Similarly, you can include attachments (like assets as support material for a tutorial) by placing them into a `files/` folder next to the .rst file, and using this inline markup:

```rst
:download:`myfilename.zip <files/myfilename.zip>`
```

## Building with Sphinx

To build the HTML website (or any other format supported by Sphinx, like PDF, EPUB or LaTeX), you need to install [Sphinx](https://www.sphinx-doc.org/) >= 1.3 as well as (for the HTML) the [readthedocs.org theme](https://github.com/snide/sphinx_rtd_theme). You also need to install the Sphinx extensions defined in `requirements.txt`.

Those tools are best installed using [pip](https://pip.pypa.io), Python's module installer. The Python 3 version might be provided (on Linux distros) as `pip3` or `python3-pip`. You can then run:

```sh
pip install -r requirements.txt
```

You can then build the HTML documentation from the root folder of this repository with:

```sh
make html
```

You can then test the changes live by opening `_build/html/index.html` in your favorite browser.

### Building with Sphinx on Windows

On Windows, you need to:

* Download the Python installer [here](https://www.python.org/downloads/).
* Install Python. Don't forget to check the "Add Python to PATH" box.
* Use the above `pip` commands.

Building is still done at the root folder of this repository using the provided `make.bat`:

```sh
make.bat html
```

Alternatively, you can build with this command instead:

```sh
sphinx-build -b html ./ _build
```

Note that during the first build, various installation prompts may appear and ask to install LaTeX plugins. Make sure you don't miss them, especially if they open behind other windows, else the build may appear to hang until you confirm these prompts.

You could also install a normal `make` toolchain (for example via MinGW) and build the docs using the normal `make html`.

### Building with Sphinx and virtualenv

If you want your Sphinx installation scoped to the project, you can install it using virtualenv. Execute this from the root folder of this repository:

```sh
virtualenv --system-site-packages env/
. env/bin/activate
pip install -r requirements.txt
```

Then do `make html` like above.

## License

All the content of this repository is licensed under the Attribution-ShareAlike 4.0 International license ([CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)) and is to be attributed to "Brett Kromkamp". See [LICENSE](/LICENSE) for details.
