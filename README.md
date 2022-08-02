# python

# String format
```
f'{0} '.format(myval)
f'{array[0]}'


print('ma chaine ' + chaine1 )

# number with nb number after comma .
print('nombre %1.2f' % (123.123456))
nombre 123.12

print('ma chaine %s' % ('est ici'))
ma chaine est ici

print('chaine=%s - number=%1.2F' % ('machaine', 1234.456))
chaine=machaine - number=1234.46
```

* See: https://github.com/davidboukari/jenkins-test-pipeline/blob/dev2/README.md
## install the Package
```
pip install tox
pip install setuptools 
pip install setuptools 
pip install --upgrade pip
pip install corage
pip install coverage
pip install pytest-cov
pip install flake8
pip install prettyprinter 
pip install pylint
pip install setuptools
pip install wheel 
```

## pytest Coverage
```
pytest -v --tb=short  --cov=app -cov-branch --cov-report xml:coverage.xml --junitxml report.xml 
```

### flake8
```
 flake8 --max-line-length=150 --max-complexity=10
```

## tox

```
cat tox.ini
[tox]
envlist = py38
skipsdist = True

[flake8]
max-line-length=150
max-complexity=13
#filename = app

[testenv]
deps = -r requirements.txt
commands= pytest
          flake8 app tests
          pylint app

[pytest]
addopts  = -v
           --tb=short
           --cov=app
           -cov-branch
           --cov-report xml:coverage.xml
           --junitxml report.xml
```

### Execute tox
```
tox -r
```

### Create the setup.py
```
from setuptools import setup, find_packages

setup(name="jenkins-test-pipeline",
      version="0.0.1",
      description="A pipeline test with alert managing https://github.com/davidboukari/jenkins-test-pipeline.git",
      author="David Boukari",
      author_email="davidboukari@gmail.com",
      packages=find_packages(),
      install_requires=[
            'appdirs==1.4.4',
            'astroid==2.5.6',
            ...
      ],
      license="Apache 2.0"
      )

```

```
python setup.py sdist
python setup.py bdist_wheel

```




## Upload a package to nexus
* Create the repository: https://www.nova-technology.fr/2019/03/27/repository-python/

* Create a blob python
```
Type: File
Name: pytho
```

* Configure a private repo
```
Name: pypi-hawksys
Format: pypi
Type: hosted
blob store: python
```

* Create a proxy repo of https://pypi.python.org/
```
Remote storage: https://pypi.python.org/
Blob storage: python
```

### Configure pip  and upload the package
```
cat .pypirc
[distutils]
index-servers=nexus-pypi

[nexus-pypi]
repository = http://<IP_NEXUS>:8081/repository/pypi-hawksys/
trusted-host = <IP_NEXUS>
username = admin
password = xxxxxxxxx


python setup.py sdist bdist_egg upload -r nexus-pypi
```

### Install package from a private repo
```
pip install --index-url=http://<IP_NEXUS>:8081/repository/pypi-hawksys/  --trusted-host <IP_NEXUS>  jenkins-test-pipeline
```


## Docstrings
* https://www.programiz.com/python-programming/docstrings

### Docstring a function
```
def add_binary(a, b):
    '''
    Returns the sum of two decimal numbers in binary digits.

            Parameters:
                    a (int): A decimal integer
                    b (int): Another decimal integer

            Returns:
                    binary_sum (str): Binary string of the sum of a and b
    '''
    binary_sum = bin(a+b)[2:]
    return binary_sum


print(add_binary.__doc__)
```

### Docstring a class
```
class Person:
    """
    A class to represent a person.

    ...

    Attributes
    ----------
    name : str
        first name of the person
    surname : str
        family name of the person
    age : int
        age of the person

    Methods
    -------
    info(additional=""):
        Prints the person's name and age.
    """

    def __init__(self, name, surname, age):
        """
        Constructs all the necessary attributes for the person object.

        Parameters
        ----------
            name : str
                first name of the person
            surname : str
                family name of the person
            age : int
                age of the person
        """

        self.name = name
        self.surname = surname
        self.age = age

    def info(self, additional=""):
        """
        Prints the person's name and age.

        If the argument 'additional' is passed, then it is appended after the main info.

        Parameters
        ----------
        additional : str, optional
            More info to be displayed (default is None)

        Returns
        -------
        None
        """

        print(f'My name is {self.name} {self.surname}. I am {self.age} years old.' + additional)
```
