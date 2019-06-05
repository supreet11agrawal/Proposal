Contributing
=============

## Table Of Contents
* Basic Work Flow
* Coding Conventions
* Setting Up
  * Fork Itzamna
  * Clone Itzamna
  * Installing Requirements
* Work Flow Process
  * Create a new branch
  * Modify Code
  * Commit the changes
    * Writing Commit Messages
  * Creating Pull Request
    * Update Pull Request


## Basic Work Flow ##

1. Create a new branch
2. Modify code
3. Be sure that code is working as expected
4. Commit the changes
5. Create a Pull Request on Github.

Make sure to synchronize with the master branch after submitting the patch.


## Coding Conventions ##


Follow the standard Style Guide for Python Code when writing code, as explained at the following URLs:

* [PEP 8 -- Style Guide for Python Code](http://www.python.org/dev/peps/pep-0008)
* [PEP 257 -- Docstring Conventions](http://www.python.org/dev/peps/pep-0257)

In particular,

- Use 4 spaces for indentation levels.

- Use all lowercase function names with words separated by
  underscores. For example, you are encouraged to write Python
  functions using the naming convention


      def set_some_value()

  instead of the CamelCase convention.

- Use CamelCase for class names and major functions that create
  objects, e.g.


      class HelloWorld(object)

## Setting Up ##



### Fork Itzamna ###


Go to the Itzamna Github repository:

- [Hackcave/Itzamna](https://github.com/hackcave/itzamna)

and click the "Fork" button.


### Clone Itzamna ###

On your machine browse to where you would like to store Itzamna, and clone
the latest code from your forked repository:

    $ git clone git://github.com/your_username/itzamna.git
    $ cd itzamna

Then assign your read-and write repo to a remote called "github":

    $ git remote add github git@github.com:hackcave/itzamna.git

You can observe the remote names with the help of this command:
    
    $ git remote -v
    origin  git@github.com:your_username/itzamna.git (fetch)
    origin  git@github.com:your_username/itzamna.git (push)
    github  git@github.com:hackcave/itzamna.git (fetch)
    github  git@github.com:hackcave/itzamna.git (push)


### Installing Requirements ###


Use virtual environment to isolate the development version.

You can set up virtual environments using [virtualenv](https://virtualenv.pypa.io)
or [conda](http://conda.pydata.org/). Conda has the advantage that all software
installs are binary and that you can easily switch between python versions. Here
is an example of using conda to create two development virtual environments, one
for python 3.5 and one for python 3.7:

    $ conda create -n itzamna-dev-py35 python=3.5
    $ conda create -n itzamna-dev-py37 python=3.7

To activate the Python 3.7 environment, use:

    $ conda activate itzamna-dev-py37

To install requirements, use:

	  $ pip install -r requirements.txt


## Workflow Process ##


### Create a new branch ###

Remember, never begin your work in master. While it is technically possible to
make your git workflow regardless of the name of branch, it would be the best
to avoid because it would be too difficult to manage your workflow. You should name
the branch describing the topic of the change.

Also, **never** type the following commands in master: `git merge`, `git add`,
`git commit`, `git rebase`. If you had made some commits to your local master by
accident, you would either have to hard reset or rebase to drop the commits.


To create and checkout(that is, make it the working branch) a new branch, say `branch_ab`:

    $ git branch branch_ab
    $ git checkout branch_ab

or in one command using:

    $ git checkout -b branch_ab


To view all the branches, with your current branch highlighted, type:

    $ git branch


### Modify Code ###


All new methods, functions and classes should have docstrings showing the basic
working and usage.

Keep the code clean and follow the coding conventions explained above.


### Commit the changes ###


You can check what files are changed:
    
    $ git status

Check total changes:

    $ git diff

Add new files to the indx if necessary:

    $ git add new_file.py

After everything is okay, you are ready to commit the changes locally. A commit also
contains a commit message which describes it. To commit the changes locally, type:

    $ git commit


#### Writing Commit Messages ####

**Title** 


The title of your commit message should summarise what the commit does. try to avoid
short commit messages, like "Fix" or messages that give no context, like "Found the bug".

Tools like `git`, `shortlog` or even GitHub only show the first line of the commit by default,
so it is important to convey the most important aspects of the commit in the first line.

* Keep to 71 characters or less.
* Do not end with a period.
* Provide context for the commit if possible.

**Body**


Commit messages are intended for human readers, both for people who will be reviewing
your code right now, and for people who might come across your commit in the future
while researching some change in the code. Thus, include information that helps others 
understand your commit here, if necessary.

* **Make sure to leave a blank line after the summary**
* Keep all lines to 78 characters or less
  (so they can be easily be read in terminals which don't automatically wrap lines.)
* Give an overview of what the commit does if it is difficult to figure out just 
  from looking at the diff. 
* Include other relevant information, e.g.

  * Known issues
  * A concrete example (for commits that add new features/improve performance etc.)

* Use bullet lists when suitable
* Use plain English


### Create a pull request ###


Be sure that you are in your own branch, and run:

    $ git push github branch_ab

#### Update pull request ####


If you need to make changes to a pull request there is no need to close it. The best
way to make a change is to add a new commit in your local repository and simply repeat
push command:

    $ git commit
    $ git push github branch_ab

Note that if you do any rebasing or in any way edit your commit history, you will have
to add the -f (force) option to the push command for it to work:

    $ git push -f github


