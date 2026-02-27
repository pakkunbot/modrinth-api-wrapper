Use Ubuntu 20.04

Install Python 3.8:

- apt update
- apt install software-properties-common
- add-apt-repository ppa:deadsnakes/ppa
- apt install python3.8
- python3 --version

Install Pip:

- apt-get install wget
- wget https://bootstrap.pypa.io/pip/3.8/get-pip.py
- python3 get-pip.py

Build and install package:

- apt install -y libxml2-dev libxslt1-dev build-essential gcc
- pip install python-dateutil
- python3 -m build --sdist
- python3 -m pip install dist/*.tar.gz

Setup ~/.pypirc:

```
[pypi]
  username = __token__
  password = <api_token>
```

Publish package:

- pip install twine
- twine upload dist/*
