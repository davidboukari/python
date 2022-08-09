# python

# help
```
ex: help(list.reverse)
Help on method_descriptor:
reverse(self, /)
    Reverse *IN PLACE*.
```

* Get keyboard input

```
chaine = input('Please give an integer')
print(chaine)
Please give an integer>? salut toi
salut toi

val = int(input('Please give an integer'))

# while True
def askIntegerRob():
    while True:
        try:
            val = int(input('Please give an integer'))
        except:
            print('It is not an Integer')
            continue
        else:
            print('it is an integer')
            break
        finally:
            print('Always executed')
    print(val)
```


# type
```
type([])
<class 'list'>
type({})
<class 'dict'>
type(list)
<class 'type'>
str='abc'
type(str)
<class 'str'>
```

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
.keys() or .values()

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
* Function not in an object
* Methode in object  object.methode()
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


help(list.reverse)
Help on method_descriptor:
reverse(self, /)
    Reverse *IN PLACE*.
    
    
# LEGB Local Enclosing Global Built-in  function always can get Global var
Order is
* Local domain of the function
* Domain of the caller
* global domain
* domain var buit-in python

# use global to be sur to access a global var in a functionglobal mavar 
# To see all global vars: globals()
globals()
{'__name__': '__main__', '__doc__': None, '__package__': '', ..., 


# Lambda expressions: Quick function
def square(num):
    '''
    Return the num^2  => num**2
    :param num: the number
    :return: the square of the number
    '''
    return num**2
square(2)
4

In lambda expression
carre = lambda num: num**2
carre(2)
4

pair = lambda x: x % 2 == 0
pair(3)
False
pair(6)
True

first_char = lambda string: string[0]
first_char('Bonjour')
'B'

verlan = lambda string: string[::-1]
verlan('Bonjour')
'ruojnoB'

add = lambda x,y: x+y
add(2,3)
5

```

# object => class  for a class the 1st later should be Uppercase
```
class MyCclass(param): 
  self


class Example(object):
    pass
myobj = Example()
type(myobj)
<class '__main__.Example'>

class Chien(object):
    def __init__(self, race):
        self.race = race
sam = Chien(race='Labrador')
sam
<__main__.Chien object at 0x7fe97a633790>

sam.race
'Labrador'


class Chien(object):
    # Class attribute
    espece = 'mamifere'
    
    def __init__(self, race, nom):
        self.race = race
        self.nom = nom
        
        
class Cercle(object):
    '''
    Class Cercle to draw and manage a circle
    '''
    # Class Attributes
    pi = 3.14

    def __init__(self, rayon=1):
        self.rayon = rayon

    def surface(self):
        '''
        Calculate the surface of the circle
        :return:
        '''
        return Cercle.pi * self.rayon**2

    def definirRayon(self, rayon):
        '''
        Set the rayon of the circle
        :param rayon: rayon of the circle
        :return:
        '''
        self.rayon = rayon

    def obtenirRayon(self):
        '''
        Get the rayon
        :return:
        '''
        return self.rayon
        
        
class Animal(object):
    '''
    Class Animal ...
    '''
    def __init__(self):
        print('Animal created')
    def whoiam(self):
        print('i am an animal')
    def eat(self):
        print('i am eating')
        
a = Animal()
Animal created
a.whoiam()
i am an animal
a.eat()
i am eating


class Chien(Animal):
    '''
    Class Chien (extends of Animal)
    '''
    def __init__(self):
        Animal.__init__(self)
        print('Dog created')
    def whoiam(self):
        print('I am a dog')
    def aboie(self):
        print('ouaf ouaf !!!')
        
c = Chien()
Dog created
c.whoiam()
I am a dog
c.aboie()
ouaf ouaf !!!
c.eat()
i am eating

# Special Method
## __str__ called by print()  when we want to print an object
class Livre(object):
    '''
    '''
    def __init__(self, title, author, pages):
        self.title = title
        self.author = author
        self.pages = pages
        print('Book is created')
    def __str__(self):
        return 'Title: %s, Author: %s, Pages: %i' % (self.title, self.author, self.pages)
    
o = Livre('Les femmes savantes', 'Moliere', 123)
Book is created
o
<__main__.Livre object at 0x7fe97a64d990>
print(o)
Title: Les femmes savantes, Author: Moliere, Pages: 123

## __len__ called by len()
class Livre(object):
    '''
    '''
    def __init__(self, title, author, pages):
        self.title = title
        self.author = author
        self.pages = pages
        print('Book is created')
    def __str__(self):
        return 'Title: %s, Author: %s, Pages: %i' % (self.title, self.author, self.pages)
    def __len__(self):
        return self.pages
    
o = Livre('Les femmes savantes', 'Moliere', 123)
Book is created
print(o)
Title: Les femmes savantes, Author: Moliere, Pages: 123
len(o)
123


## del when delete an object
class Livre(object):
    '''
    '''
    def __init__(self, title, author, pages):
        self.title = title
        self.author = author
        self.pages = pages
        print('Book is created')
    # Called by print
    def __str__(self):
        return 'Title: %s, Author: %s, Pages: %i' % (self.title, self.author, self.pages)
    # Called by len
    def __len__(self):
        return self.pages
    # Called by delete object
    def __del__(self):
        print('Delete the book')
        
o = Livre('Les femmes savantes', 'Moliere', 123)
Book is created
del o

```

## Modules & Packages
* https://docs.python.org/3/tutorial/modules.html
```
import math
math.pi
3.141592653589793
math.sqrt(2)
1.4142135623730951
pi
Traceback (most recent call last):
  File "/Library/Frameworks/Python.framework/Versions/3.7/lib/python3.7/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<input>", line 1, in <module>
NameError: name 'pi' is not defined
math.pi
3.141592653589793
from math import pi
pi
3.141592653589793

from math import pi, sqrt
sqrt(4)
2.0


## Describe a lib with dir()
dir(math)
['__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'copysign', 'cos', 'cosh', 'degrees', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'gcd', 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'log2', 'modf', 'nan', 'pi', 'pow', 'radians', 'remainder', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau', 'trunc']


# Help
help(math.asin)
Help on built-in function asin in module math:
asin(x, /)
    Return the arc sine (measured in radians) of x.
    
    
## Package
On peut creer un package: just need to add __init__.py can be empty or 
Ex:
cat __init__.py
__all__ = ["bar"]

Can use __all__ if we do not want that all be accessible
```

## Exceptions
* Built-in list: https://docs.python.org/3/library/exceptions.html
```
try:
    2 + 'chaine'
except TypeError:
    print('Type Error')
    
Type Error

## finally
try:
    file = open("myfile.txt", 'w')
    file.write("A line")
except IOError:
    print("IO Error")
else:
    print("line wrote")
    file.close()
line wrote

try:
    file = open('myfile1.txt','r')
    line = file.read()
except:
    print('Error')
finally:
    print('This message is always printed')
    
Error
This message is always printed

# while True
def askIntegerRob():
    while True:
        try:
            val = int(input('Please give an integer'))
        except:
            print('It is not an Integer')
            continue
        else:
            print('it is an integer')
            break
        finally:
            print('Always executed')
    print(val)
```

## Integrated functions
* Map(funcction, listIterable)  apply a function to a list (iterable)
```
help(map)
Help on class map in module builtins:
class map(object)
 |  map(func, *iterables) --> map object

def farenheit(temp):
    return float(9/5) * temp + 32
def celsius(temp):
    return float(5/9) * (temp - 32)
farenheit(37)
98.60000000000001
celsius(100)
37.77777777777778
temp = [ 0, 22.5, 40, 100]
F_temp = list(map(farenheit, temp))
F_temp
[32.0, 72.5, 104.0, 212.0]

list(map(lambda x: float(5/9) * (x - 32), F_temp))
[0.0, 22.5, 40.0, 100.0]
```

## filter(function, iterable)  filter a list
```
def is_pair(x):
    if x % 2 == 0:
        return True
l  = range(0,10)
l
range(0, 10)
print(l)
range(0, 10)
list(l)
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
filter(is_pair, l)
<filter object at 0x7fe97a68c910>
list(filter(is_pair, l))
[0, 2, 4, 6, 8]

list(filter(lambda x: x % 2 == 0, l))
[0, 2, 4, 6, 8]
```

## enumerate  => return a list with index number order
```
l = [ 'a', 'b', 'cc']
for n, item in enumerate(l):
    print(n,item)
    
0 a
1 b
2 cc

for n, item in enumerate(l):
    if n > 1:
        break;
    else:
        print(item)
        
a
b


```

## all & any
* all => return True if all if True
* any return True if at least 1 element is True
```
l = [True, True, False, True]
all(l)
False
any(l)
True
```

## complex
```
complex(2,3)
(2+3j)
complex(2,3) + complex(4,5)
(6+8j)

complex('2+3j')
(2+3j)
```

## zip tranforme list to dico  stop to the lower list
```
l1=[1,2,3]
l2=[4,5,6]
list(zip(l1,l2))
[(1, 4), (2, 5), (3, 6)]
l3=[7,8,9]
list(zip(l1,l2,l3))
[(1, 4, 7), (2, 5, 8), (3, 6, 9)]

[(1, 4, 7), (2, 5, 8), (3, 6, 9)]
l4=[10,11,12,13,14,15]
list(zip(l1,l4))
[(1, 10), (2, 11), (3, 12)]

# with dico
d = dict(zip(l1,l2))
d
{1: 4, 2: 5, 3: 6}


key={'chat', 'chien'}
value={'miaou','waf'}
dict(zip(key,value))
{'chien': 'waf', 'chat': 'miaou'}


```

## Decorator function in funcction
* Call function in functon
* Give a function as parameter
```
globals().keys()

dict_keys(['__name__', '__doc__', '__package__', '__loader__', '__spec__', '__file__', '__builtins__', 'sys', 'square', 'carre', 'pair', 'first_char', 'verlan', 'add', 'str', 'Example', 'myobj', 'Chien', 'sam', 'Cercle', 'c', 'Animal', 'a', 'Livre', 'math', 'pi', 'sqrt', 'file', '__warningregistry__', 'askInteger', 'askIntegerRob', 'farenheit', 'celsius', 'temp', 'F_temp', 'is_pair', 'l', 'n', 'item', 'l1', 'l2', 'l3', 'l4', 'd', 'key', 'value'])


globals()['c']
<__main__.Chien object at 0x7fe97a657dd0>

globals().values()

dict_values(['__main__', None, '', ...

# copy a function to a var create a new function can delete the older without deleted the new function
def bonjour(nom='me'):
    return 'hello %s'  % nom 
bonjour
<function bonjour at 0x7fe97a64b290>
bonjour()
'hello me'
save_bonjour = bonjour
save_bonjour()
'hello me'

del bonjour
save_bonjour()
'hello me'


# Function as parameter
def bonjour():
    print('Bonjour !!!')
def autre(func):
    print('Autre call some code')
    print(func())
    
autre(bonjour)
Autre call some code
Bonjour !!!
None

```

## Iterator & Generator
* generator: yield to not create the object like list but generate when it is needed
```
def gencube(n):
    liste = []
    for x in range(n):
        liste.append(x**3)
    return liste

# No memory list stockage   with yield
def gencube2(n):
    for x in range(n):
        yield x**3

gencube(5)
[0, 1, 8, 27, 64]
gencube2(5)
<generator object gencube2 at 0x7fe97a3d0050>
list(gencube2(5)
[0, 1, 8, 27, 64]
for x in gencube2(5)
    print(x)

0
1
8
27
64

def genfibo(n):
    a = 1
    b = 1
    for x in range(0,n):
        yield a
        a,b = b, a+b
        
genfibo(10)
<generator object genfibo at 0x7fe97a3d0050>
for x in genfibo(10):
    print(x)
    
1
1
2
3
5
8
13
21
34
55


without yield
def genfibonwithoutyield(n):
    a = 1
    b = 1
    sortie = []
    for x in range(n):
        sortie.append(a)
        a,b = b, a+b
    return sortie
    
genfibonwithoutyield(10)
[1, 1, 2, 3, 5, 8, 13, 21, 34, 55]

```

## next iter
next: Access to the next element in a seq
iter: Transoform to iter
```
def gen_simple():
    for x in range(3):
        yield x
        
g = gen_simple()
print(next(g))
0
print(next(g))
1
print(next(g))
2
print(next(g))
Traceback (most recent call last):
  File "/Library/Frameworks/Python.framework/Versions/3.7/lib/python3.7/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<input>", line 1, in <module>
StopIteration


s = 'machaine'
for c in s:
    print(c)
    
m
a
c
h
a
i
n
e
next(s)
Traceback (most recent call last):
  File "/Library/Frameworks/Python.framework/Versions/3.7/lib/python3.7/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<input>", line 1, in <module>
TypeError: 'str' object is not an iterator
s_iter = iter(s)
next(s)
Traceback (most recent call last):
  File "/Library/Frameworks/Python.framework/Versions/3.7/lib/python3.7/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<input>", line 1, in <module>
TypeError: 'str' object is not an iterator
next(s_iter)
'm'
next(s_iter)
'a'
next(s_iter)
'c'
next(s_iter)
'h'
next(s_iter)
'a'
next(s_iter)
'i'
next(s_iter)
'n'
next(s_iter)
'e'
next(s_iter)
Traceback (most recent call last):
  File "/Library/Frameworks/Python.framework/Versions/3.7/lib/python3.7/code.py", line 90, in runcode
    exec(code, self.locals)
  File "<input>", line 1, in <module>
StopIteration

```

## Counter
* counter(list) return a list with nb occ each element
```
liste=[1,2,5,3,2,6,2,1,4,6,7,7,7,9]
Counter(liste)
Counter({2: 3, 7: 3, 1: 2, 6: 2, 5: 1, 3: 1, 4: 1, 9: 1})

Counter('abcdaefbdg')
Counter({'a': 2, 'b': 2, 'd': 2, 'c': 1, 'e': 1, 'f': 1, 'g': 1})

phrase='combien de fois on trouve des mots dans cette phrase avec de mot, oui combien'
list_mot = phrase.split()
list_mot
['combien', 'de', 'fois', 'on', 'trouve', 'des', 'mots', 'dans', 'cette', 'phrase', 'avec', 'de', 'mot,', 'oui', 'combien']
Counter(list_mot)
Counter({'combien': 2, 'de': 2, 'fois': 1, 'on': 1, 'trouve': 1, 'des': 1, 'mots': 1, 'dans': 1, 'cette': 1, 'phrase': 1, 'avec': 1, 'mot,': 1, 'oui': 1})


```

## pdb
```
import pdb
x = [1,2,3]
y = 10
z = 20
a = y + z
pdb.set_trace()
print(a)
b = x + y
> <input>(7)<module>()
(Pdb) >? x
[1, 2, 3]
(Pdb) >? y
10
(Pdb) >? x+y
*** TypeError: can only concatenate list (not "int") to list
(Pdb) >? display x
display x: [1, 2, 3]
(Pdb) >? whatis x
<class 'list'>
(Pdb) 

(Pdb) >? help
Documented commands (type help <topic>):
========================================
EOF    c          d        h         list      q        rv       undisplay
a      cl         debug    help      ll        quit     s        unt      
alias  clear      disable  ignore    longlist  r        source   until    
args   commands   display  interact  n         restart  step     up       
b      condition  down     j         next      return   tbreak   w        
break  cont       enable   jump      p         retval   u        whatis   
bt     continue   exit     l         pp        run      unalias  where    
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
