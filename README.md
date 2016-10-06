Setting up Sphinx and Bootstrap in gh-pages
==================================

*Heavily based on this [LA Times article](http://datadesk.latimes.com/posts/2012/01/sphinx-on-github/)*.

##Part 1: Making gh-pages:
* `git checkout --orphan gh-pages`
* `git rm -rf .`

##Part 2: Setting up Sphinx:
* Install the Sphinx Python package (e.g. `pip install sphinx`).
* `cd` into your main repo directory, make sure you're on the gh-pages branch.
* At the command line, enter `touch .nojekyll`
* At the command line, enter `sphinx-quickstart`
* Use the defaults for all the prompts, **except** for the second prompt where you must enter 'Y'.
  * You should probably also enter something for your project and author names, and set the version to be whatever you want (1.0, 0.0.1, etc).
* Open the 'Makefile' in the text editor of your choice:
  * `BUILDDIR = ./` (8th line in Sphinx 1.2.3).
  * `$(SPHINXBUILD) -b html $(ALLSPHINXOPTS) $(BUILDDIR)` (53rd line in Sphinx 1.2.3).
* .rst (Markdown) files are in `source/`, type `make html` to build website (index in root project directory).

##Part 3 (optional): Making it pretty with Bootstrap:
* Install the sphinx-bootstrap-theme Python package (e.g. `pip install sphinx-bootstrap-theme`).
* Edit `source/conf.py` to look like the one in this repo, replacing text where appropriate for your project.
  * Optionally, you can link to a logo graphic you store in `source/_static/`
* The theme we've chosen has the navigation links at the top of the page by default, which is not always optimal. You can get around this by overriding the layout. Look in `source/_templates/layout.html` in this repo to see how to add the nav links to the page footer. (This repo's `layout.html` override also includes some fields in the header of the pages to enable video embedding. Feel free to ignore that block if you don't want to use video.)

##Part 4: Viewing the results!
Once you're done with all of these steps, commit and push your changes to GitHub. The index page of your website will now be visible at 'https://github.com/pages/[USER]/[REPO]/'. You can now start adding pages to your site! See [here](http://sphinx-doc.org/contents.html) for the Sphinx documentation, which has a guide to the markdown language Sphinx uses as well as information on how to link pages together through table-of-contents-trees (toctrees, for short).
