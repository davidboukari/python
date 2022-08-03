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

# auto conversion %r
print('chaine=%r - number=%r' % ('machaine', 1234.456))
chaine='machaine' - number=1234.456

# format
print('{p} toi !!! {p} à vous !!!'.format(p='Bonjour'))
Bonjour toi !!! Bonjour à vous !!!

print('{a} toi !!! {b} à vous !!!'.format(a='Bonjour', b=123))
Bonjour toi !!! 123 à vous !!!

ma_liste + ['new element']
['une chaine', 245.23124, 'o', 'new element']


ma_liste = ma_liste + ['new element']
ma_liste
['une chaine', 245.23124, 'o', 'new element']

ma_liste * 2
['une chaine', 245.23124, 'o', 'new element', 'une chaine', 245.23124, 'o', 'new element']
```

## List [] => [1, 'element', 'test', 12.567 ] elements are indexed by number
```
ma_liste=['une chaine',245.23124,'o']
len(ma_liste)
3
ma_liste[0]
'une chaine'

print(ma_liste)
['une chaine', 245.23124, 'o']

print(*ma_liste)
une chaine 245.23124 o

print(*ma_liste, sep=',')
une chaine,245.23124,o

ma_liste[1:]
[245.23124, 'o']

# Append or pop element in the list
list1=[1,2,3]
list1.append(4)
list1
[1, 2, 3, 4]
list1.pop(2)
3
list1
[1, 2, 4]

# pop with no parameter extract and remove the lastlist1.pop()
4
list1
[1, 2]

list1=[1,2,3]
list1
[1, 2, 3]
list1.reverse()
list1
[3, 2, 1]

list2=['z','a','d','b']
list2.sort()
list2
['a', 'b', 'd', 'z']

# matrice
l1=[1,2,3
l2=[4,5,6
l3=[7,8,9]
matrice=[l1,l2,l3]
matrice
[[1, 2, 3], [4, 5, 6], [7, 8, 9]
matrice[0]
[1, 2, 3]

matrice[1][2]
6

# list comprehension
col = [ ligne[0] for ligne in matrice]
col
[1, 4, 7]
```


## Dico {} => {'ele1':'val1', 'test':'no' }hash table elements are indexed by index name
```
dico={'cle1':'val1', 'cle2':'val2'}
dico
{'cle1': 'val1', 'cle2': 'val2'}

dico['cle2']
'val2'

dico={'cle1':123, 'cle2':[12,234.21,45], 'cle3':['item0', 'item1']}
dico
{'cle1': 123, 'cle2': [12, 234.21, 45], 'cle3': ['item0', 'item1']}

dico={'cle1':123, 'cle2':[12,234.21,45], 'cle3':['item0', 'item1']}
dico
{'cle1': 123, 'cle2': [12, 234.21, 45], 'cle3': ['item0', 'item1']}
dico['cle3']
['item0', 'item1']
dico['cle3'][1]
'item1'

dico['cle3'][1].upper()
'ITEM1'

dico['cle1']
123
dico['cle1'] -= 23
dico['cle1']
100

dico={}
dico['reponse']='chien'
dico
{'reponse': 'chien'}

dico={'cle1':1, 'cle2':2, 'cle3':3}
dico
{'cle1': 1, 'cle2': 2, 'cle3': 3}
dico.keys()
dict_keys(['cle1', 'cle2', 'cle3'])
dico.values()
dict_values([1, 2, 3])

## tuples
dico.items()
dict_items([('cle1', 1), ('cle2', 2), ('cle3', 3)])
```

## Set remove double and sort 
```
my_set=set()
my_set
set()
my_set.add(1)
my_set.add(2)
my_set
{1, 2}

list3=[9,1,5,10,3,2]
set(list3)
{1, 2, 3, 5, 9, 10}
```

## Boolean
```
bol=True
bol
True
1>2
False
```


## Tuples () => (1,2,3) Immutable (cannot be updated) - no reaffectation - no append
```

tup=["un",2,'trois']

# Get the index of a search value
tup.index('un')
0
tup.index(2)
1

# nb occc
tup=["un",2,'trois',2,4,'aa',2]
tup.count(2)
3


```
## Files open() : default is ro  => the + permit to update ex: w+ read,write a+: Read write append
```
file = open('test.txt')
file.read()
'This is a test\n'

file.seek(0)
0
file.read()
'This is a test\n'


#Get a list off all lines
file.seek(0)
0
file.readlines()
['This is a test\n']


#Read Write 
file = open('test.txt','w+')
file.write('new line')
8
file.readlines()
[]
file.seek(0)
0
file.readlines()
['new line']

#for all lines
for line in open('test.txt'):
    print(line)
    
line1 ...
line2...


file.seek(0)
0
print(file.read())
line1 ...
line2...


file.seek(0)
0
content = file.readlines()
print(content)
['line1 ...\n', 'line2...\n']

# do not forget to close
file.close()

# With syntax
with open('test.txt') as file:
    content = file.read()
    
content
'line1 ...\nline2...\n'

# Append
file = open('test.txt','a+')
file.write('new line')
8
file.seek(0)
0
file.readlines()
['line1 ...\n', 'line2...\n', 'new line']

```

## if elif else
```
if 2 > 1:
    print('case 1')
elif 5 < 7:
    print('case 2')
else:
    print('case 3')


bool=False
if bool:
    print('bool is true')
else:
    print('bool is false')
bool is false

lieu = 'Bank'
if lieu == 'Shop':
    print('Welcome to the Shop')
elif lieu == 'Bank':
    print('Welcome to the bank')
else:
    print('Where are you?')
Welcome to the bank
```

## for
```
liste = [1,2,3,4]
for num in liste:
    print('This is the number: %i' % (num))
This is the number: 1
This is the number: 2
This is the number: 3
This is the number: 4


liste = [ 1, 2, 3, 4, 5, 6]
for num in liste:
    if num % 2 == 0:
        print('%i is pair' % num)
    else:
        print('%i is impair' % num)
    
1 is impair
2 is pair
3 is impair
4 is pair
5 is impair
6 is pair

comp=0
for num in liste:
    comp += num
print('Total is: %i' % comp)
Total is: 21

liste_of_tuple=[(1,2),(3,4),(5,6,7)]
liste_of_tuple
[(1, 2), (3, 4), (5, 6, 7)]
for elem in liste_of_tuple:
    print(elem)
(1, 2)
(3, 4)
(5, 6, 7)

liste_of_tuple=[(1,2),(3,4),(5,6)]
for (m,n) in liste_of_tuple:
    print(n)
2
4
6

#print dico
dico={'cle1': 1, 'cle2': 2, 'cle3': 3}
for item in dico:
    print(item)
cle1
cle2
cle3
for (cle,val) in dico.items():
    print(cle)
    print(val)
cle1
1
cle2
2
cle3
3

```

# while
```
while test:
  action
else:
  action when false
  
while x < 4:
    print(x)
    x += 1
    
0
1
2
3

# finished
x = 0
while x < 4:
    print(x)
    x += 1
else:
    print('Completed')
0
1
2
3
Completed


x = 0
while x < 5:
    print(x)
    x += 1
    if(x == 3):
        print('Ok x == 3')
        break;
    else:    
        continue
0
1
2
Ok x == 3

```

## Range default start = 0 (evantail) range(start, nbnumber)
```
list(range(0,10) ) is same as list(range(10))

list(range(0,10))
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

my_range = range(0,10)
type(my_range)
<class 'range'>

start=0
stop=20
list(range(start,stop))
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]

# witth step
start=0
stop=20
step=2
list(range(start,stop,step))
[0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
```

## List in comprehension
```
liste = [ x for x in 'example']
liste
['e', 'x', 'a', 'm', 'p', 'l', 'e']

['e', 'x', 'a', 'm', 'p', 'l', 'e']
liste = [ x for x in range(0,11)]
liste
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Square
liste = [ x**2 for x in range(0,11)]

# Pair
liste = [ x for x in range(0,11) if x % 2 == 0]
liste
[0, 2, 4, 6, 8, 10]
liste
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

## Root Square
liste = [ x**0.5 for x in range(0,11) if x % 2 == 0]
liste
[0.0, 1.4142135623730951, 2.0, 2.449489742783178, 2.8284271247461903, 3.1622776601683795]


# Convert °C to °F
celcius = [ 0, 10, 20.1, 34.5]
farenheint = [ (9/5) * temp + 32 for temp in celcius]
farenheint
[32.0, 50.0, 68.18, 94.1]
```

## Functions  => def my_function(param0, param1, ..., paramn):
```
def my_function(param0, param1, ..., paramn):
  '''
  doc function
  '''
  
* Built-in functions https://docs.python.org/3/library/functions.html  

def ajoute(nbr1, nbr2):
  return nbr1 + nbr2


# Low typage
def ajoute(nbr1, nbr2):
    return nbr1 + nbr2
ajoute(1,2)
3
ajoute('un','deux')
'undeux'


def is_first(num):
    '''
    :param num: number to test
    :return: True or False
    '''
    for x in range(2, num):
        if num % x == 0:
            print('%r is not first' % num)
            return False
            break
    else:
        print('%r is First' % num)
        return True
is_first(11)
11 is First
True
is_first(6)
6 is not first
False

import math
def is_first_quick(num):
    '''
    Test if the number is first
    :param num: the number to test
    :return: Boolean
        True: if num is first
        False: if num is not first
    '''
    # Test all pair
    if num % 2 == 0:
        return False
    # Test impair
    for x in range(3,int(math.sqrt(num)) + 1, 2):
        if num % x == 0:
            return False
    return True
is_first_quick(11)
True
is_first_quick(6)
False
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
