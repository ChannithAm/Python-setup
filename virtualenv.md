* Virtualenv និង pip
** Build, python-dev and pip
>sudo apt-get install build-essential
>sudo apt-get install python-dev
>sudo apt-get install python3-dev

** Next I install Ubuntu 16.04 versions of pip both python 2 and python 3
>sudo apt-get install python-pip
>sudo apt-get install python3-pip

** Install `virtualenv, virtualenvwrapper`
>pip install --user virtualenv
>pip install --user virtualenvwrapper

** Setup `virtualenvwrapper` by making some additions to `~/.bashrc` at the end of the file and source the file (#source ~/.bashrc) or restart the terminal
```
# where to store our virtual envs
export WORKON_HOME=$HOME/virtenvs
# where projects will reside
export PROJECT_HOME=$HOME/Projects-Active
# where is the virtualenvwrapper.sh
source $HOME/.local/bin/virtualenvwrapper.sh
```
These settings

    Save virtual environments in the ~/virtenvs directory,
    Create new projects in ~/Projects-Active/new_project directory,
    Specify the location of the virtualenvwrapper.sh file– you can find this with
</br>
>which virtualenvwrapper.sh
```
/home/cn/.local/bin/virtualenvwrapper.sh
```

** First, create a python 2 virtual environment using the `virtualenvwrapper` tools
>mkvirtualenv py2 -p /usr/bin/python2
```
Running virtualenv with interpreter /usr/bin/python2
New python executable in /home/cn/virtenvs/py2/bin/python2
Also creating executable in /home/cn/virtenvs/py2/bin/python
Installing setuptools, pip, wheel...done.
virtualenvwrapper.user_scripts creating /home/cn/virtenvs/py2/bin/predeactivate
virtualenvwrapper.user_scripts creating /home/cn/virtenvs/py2/bin/postdeactivate
virtualenvwrapper.user_scripts creating /home/cn/virtenvs/py2/bin/preactivate
virtualenvwrapper.user_scripts creating /home/cn/virtenvs/py2/bin/postactivate
virtualenvwrapper.user_scripts creating /home/cn/virtenvs/py2/bin/get_env_details
```

> python -V
```
Python 2.7.12
```
>pip -V
```
pip 9.0.1 from /home/cn/virtenvs/py2/local/lib/python2.7/site-packages (python 2.7)
```

** Second, create a python 3 virtual environment using the `virtualenvwrapper`
>mkvirtualenv py3 -p /usr/bin/python3
```
Running virtualenv with interpreter /usr/bin/python3
Using base prefix '/usr'
New python executable in /home/cn/virtenvs/py3/bin/python3
Also creating executable in /home/cn/virtenvs/py3/bin/python
Installing setuptools, pip, wheel...done.
virtualenvwrapper.user_scripts creating /home/cn/virtenvs/py3/bin/predeactivate
virtualenvwrapper.user_scripts creating /home/cn/virtenvs/py3/bin/postdeactivate
virtualenvwrapper.user_scripts creating /home/cn/virtenvs/py3/bin/preactivate
virtualenvwrapper.user_scripts creating /home/cn/virtenvs/py3/bin/postactivate
virtualenvwrapper.user_scripts creating /home/cn/virtenvs/py3/bin/get_env_details
```

>python -V
```
Python 3.5.2
```
>pip -V
```
pip 9.0.1 from /home/cn/virtenvs/py3/lib/python3.5/site-packages (python 3.5)
```
** Workon, deactivate
>workon
```
py2
py3
```
>workon py2
(py2)$ python -V
```
Python 2.7.12
```
>deactivate
```
$
```

** Remove an environment in the `workon`
>deactivate
>rmvirtualenv ENV_NAME

------------------------------------------------

## Sphinx Doc

** Create a repository on Github, call it ccna-khmer

>git clone git@github.com:ChannithAm/ccna-khmer.git

>cd ccna-khmer

>mkdir first-docs-------not use

>sphinx-quickstart



install sphinx
> apt-get install python-sphinx

create directory

> mkdir Doc

Change to Doc directory
> cd Doc

> sphinx-quickstart

-- Separate source and build directories : `y`

-- Name prefix: `n`

-- Project name: <>

-- use epub: `y`

-- autodoc: `y`

-- doctest: `n`

-- intersphinx: `y`

-- write todo: `n`

-- ifconfig: `y`

Theme:
pip install sphinx_rtd_theme

In your conf.py file:

import sphinx_rtd_theme
html_theme = "sphinx_rtd_theme"
html_theme_path = [sphinx_rtd_theme.get_html_theme_path()]



References
===========
https://daler.github.io/sphinxdoc-test/includeme.html
https://channitham.github.io/ccna-khmer/
http://datadesk.latimes.com/posts/2012/01/sphinx-on-github/
https://www.youtube.com/watch?feature=player_embedded&v=oJsUvBQyHBs

