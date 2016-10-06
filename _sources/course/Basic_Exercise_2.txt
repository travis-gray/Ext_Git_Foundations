Windows GUI Usage
=========================


Initialize the Repo
------------------------
The first thing you'll want to do is **initialize a repository** - which adds version control files into a folder so that the Github application can track everthing and detect changes. You always want to keep your repositories at the *project level* (so don't drag and drop your entire desktop in there). So if we're starting from scratch, you can do this in two ways:

1. Dragging and dropping a folder from your desktop into the Github GUI application. This creates the github tracking files inside the pre-existing folder, so you don't need to create anything new.

2. Creating a repository completely new using the plus symbol on the top left corner. You will be prompted for a Name and Local Path. This creates a named empty git repository at the path that you describe (by default, it is in your Github folder). Name it "GH_TRAINING_<YOUR GH USER ID>"

.. image:: /_static/WindowsGUI1.PNG
    :align: center
    :alt: create a repo
    :height: 400px


Make your edits
----------------------------------
Let's create an empty file in your repository. Switching over to explorer view (meaning not on the application, but just on your computer), we can see what this folder looks like. Right click anywhere in the folder and hit new file, this creates an empty text file for us to edit and track changes in.

.. image:: /_static/WindowsGUI2.PNG
    :align: center
    :alt: create a empty file to track
    :height: 400px

If we switch back to the Github app view, you'll be able to see that it automatically noticed the change (See the "Uncommitted Changes" box). Now if you remember in version control theory, there were some steps to creating the commit:
1. Untracked Changes - "Add" untracked files to the staging area, which tells Github which files to track.
2. Staging Area - "Commit" the changes to tracked files.
3. Commit created

.. image:: /_static/WindowsGUI3.PNG
    :align: center
    :alt: Application Notice
    :height: 400px

You "add" the files to track by placing check marks in the boxes next to their names. Then you can name your commit by typing the summary into the summary line (this is a required field). Once you hit "commit to master", you've made your first commit! Check it out.

Great, you've figured out how to make commits on your own! But now we want to share this with the rest of the world. To do this, you hit the publish button on the top right corner. This will create a matching repository under your username on Github. You will be able to find your files under the web address http://github.com/<your GH username>/<your repository name>. It should look something like this, but with less activity and fewer files:

.. image:: /_static/WindowsGUI4.PNG
    :align: center
    :alt: Published repository
    :height: 400px


This is the Github repository for a popular open-source project called Apache Spark. Note the number of "watches", "stars", "forks", commits, and contributors. These give you a quick sense for how popular the project is.
