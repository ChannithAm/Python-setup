## . Install packages

Install appropriate packages for you dirstribution. For Debian and Ubuntu:
```
sudo apt update
sudo apt install python python-dev python3 python3-dev
```

## . Install pip

You will also need `pip`
```
wget https://bootstrap.pypa.io/get-pip.py
sudo python get-pip.py
```

Afterwards, you should have pip:
```
$ pip --version
pip 9.0.1 from /usr/local/lib/python2.7/dist-packages (python 2.7)

```

## . Installing and using virtualenv

`virtualenv` (virtual environment) is a tool that creates isolates Python environments.
```
sudo pip install --upgrade virtualenv
```

After you install virtualenv, you can create a virtualenv in you project. Use the `--python` flag to tell virtualenv which Python version to use:
```
cd your-project
virtualenv --python python3 env
```

virtualenv will create a virtual coopy of the entire Python installation in the `env` folder.

After the copoy is created, you'll need to **active** the virtualenv. Activating the virtualenv tells your shell to use the virtualenv's paths for Python.
```
source env/bin/activate
```

```
pip install google-cloud-storage
```

If you want to stop using the virtualenv and go back to your global Python, you can deactivate it:
```
deactivate
```

## . References
[1] https://cloud.google.com/python/setup

