#

# Install

Windows:

```
1. Launch Powershell in Administrator mode (right click -> Run as Administrator)
2. Go to chocolatey.org
3. Follow installation instructions
4. `choco install git -y /GitAndUnixToolsOnPath`
5. `choco install openssh -y -params "/SSHAgentFeature"`
6. `choco install atom -y`
7. `choco install python3 -y`
8. `choco install awscli -y`
9. Restart windows
10. `pip3 install boto3`
11. `pip3 install ipython`
  - If needed, install MS Visual C++ 9.0, and re-run
12. Restart windows
```


Linux
```
sudo yum install python3 -y
yum install python3-pip
pip3 install mysql-connector-python
pip3 install ipython
pip3 install boto3
```


``` bash
Create virtual env
python3 -m venv my_app/env

# activate virtual env
source ~/my_app/env/bin/activate

# install pip
pip install pip --upgrade
pip install boto3
    
```

``` python
# String constructor
str()

# Float
float()

# String constructor
int()

# List
list()

In [19]: list('Hello wolrd')
Out[19]: ['H', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'l', 'r', 'd']

# Concatenation
print("I have " + str(3) + " apples")


```


Sample Operators
``` python

# power
In [20]: 2 ** 8
Out[20]: 256
           
In [21]: greeting = 'Hello, '
           
In [23]: name = 'GuD'
                   
In [24]: greeting + name
Out[24]: 'Hello, GuD'
         
In [25]: 'na' * 5 + 'batman'
Out[25]: 'nananananabatman'
         
In [26]: 'na ' * 5 + 'batman'
Out[26]: 'na na na na na batman'
         
In [27]: [ "na" ] * 5 + [ "batman"]
Out[27]: ['na', 'na', 'na', 'na', 'na', 'batman']
         
In [28]: second_a_day = 60 * 60 * 24
         
In [29]: second_a_day
Out[29]: 86400
         
In [31]: mail_list = ['gud@me', 'thegud@3', 'some@exemple']
         
In [33]: mail_list + ['last@sss']
Out[33]: ['gud@me', 'thegud@3', 'some@exemple', 'last@sss']
         
In [35]: 3 ** 10 / 5
Out[35]: 11809.8
```


Boolean
``` python
In [36]: 'a string' == 'a srting'
Out[36]: False

In [37]: 'a string' == 'a string'
Out[37]: True

In [39]: 'a string' != 'a string'
Out[39]: False

In [40]: .1 + .1 + .1 == .3
Out[40]: False

In [41]: .1 + .1 + .1
Out[41]: 0.30000000000000004

In [43]: "apple" < "pineapple"
Out[43]: True

In [44]: 'apple' in 'pinapple'
Out[44]: True

In [45]: 'pile' in 'pinapple'
Out[45]: False

In [46]: 5 in [1,2,3,4,5]
Out[46]: True

In [47]: if "key" in "monkey": print("Oook!")
Oook!

In [48]: if "banana" in "monkey": print("Oook!")

```

Blocks

``` python
In [49]: if "monk" in "monkey":
    ...:     print("Monkey! Spit that out!")
    ...:     print("...")
    ...:     print("Yuck! Dont´t eat the monk")
    ...:
Monkey! Spit that out!
...
Yuck! Dont´t eat the monk

In [52]: name = 'GuD'

In [53]: if name < 'GuD':
    ...:     print('Go to line 1')
    ...: elif name == 'GuD':
    ...:     print('Hi GuD!')
    ...: else:
    ...:     print('Go to line 2')
    ...:
Hi GuD!

In [54]: name = 'Steve'

In [55]: if name < 'GuD':
    ...:     print('Go to line 1')
    ...: elif name == 'GuD':
    ...:     print('Hi GuD!')
    ...: else:
    ...:     print('Go to line 2')
    ...:
Go to line 2
```


Default falses

``` python
In [56]: name = ''

In [58]: if name:
    ...:     print('Hello, ' + name)
    ...: else:
    ...:     print('Type a name!')
    ...:
    ...:
Type a name!

In [59]: name = 'Bob'

In [60]: if name:
    ...:     print('Hello, ' + name)
    ...: else:
    ...:     print('Type a name!')
    ...:
    ...:
Hello, Bob

In [61]: cart = []

In [62]: if cart:
    ...:     print('Ok, check that out')
    ...: else:
    ...:     print('Empty cart')
    ...:
Empty cart

In [65]: cart = cart + ['banana']

In [66]: if cart:
    ...:     print('Ok, check that out')
    ...: else:
    ...:     print('Empty cart')
    ...:
Ok, check that out

In [67]: age = 0

In [68]: if age:
    ...:     print('You have age')
    ...: else:
    ...:     print('Type an age')
    ...:
Type an age

In [69]: age = 2

In [70]: if age:
    ...:     print('You have age')
    ...: else:
    ...:     print('Type an age')
    ...:
You have age
```


Boolean eval
``` python
In [71]: False or True
Out[71]: True

In [72]: True and False
Out[72]: False

In [73]: not True
Out[73]: False

In [74]: bool("Robin" and "Batman")
Out[74]: True

In [75]:

In [75]: bool("Robin" and "")
Out[75]: False

In [76]: "Robin" and "Batman"
Out[76]: 'Batman'

In [77]: "Robin" and 77
Out[77]: 77

In [78]: "Robin" and False
Out[78]: False

In [79]: 0 and "Batman"
Out[79]: 0

In [80]: False and "John"
Out[80]: False

In [81]: "Robin" or "Batman"
Out[81]: 'Robin'

In [82]: "Robing" or ""
Out[82]: 'Robing'

In [83]: "" or "Jhon"
Out[83]: 'Jhon'

In [84]: "" or False
Out[84]: False

In [86]: bool("" or False)
Out[86]: False

In [88]: name = "GuD"

In [90]: if name: print("Hello, " + name)
Hello, GuD

In [91]: name and print("Hello, " + name)
Hello, GuD

In [92]: name = ''

In [93]: name and print("Hello, " + name)
Out[93]: ''

In [94]: name = name or "Nemo"

In [95]: print(name)
Nemo

In [96]: name = "GuD"

In [97]: name = name or "Nemo"

In [98]: print(name)
GuD

In [99]: 5 and not "Alice"
Out[99]: False

In [100]: bool('Alice')
Out[100]: True

In [101]: print(len(name))
3

In [102]: print(len(cart))
1

In [103]: cart = cart + ['milk']

In [104]: print(len(cart))
2
```


Splicing, spliting, joining and iterating

``` python
In [105]: colors = ['red', 'orange', 'yellow', 'green', 'blue', 'purple']

In [106]: sentence = "The quick brown fox jumped over the lazy dog"

In [107]: sentence[0]
Out[107]: 'T'

In [108]: sentence[4]
Out[108]: 'q'

In [110]: colors[1]
Out[110]: 'orange'

In [111]: colors[-1]
Out[111]: 'purple'

In [112]: sentence[-3]
Out[112]: 'd'

# Start:stop before
In [113]: colors[1:4]
Out[113]: ['orange', 'yellow', 'green']

In [114]: sentence[4:9]
Out[114]: 'quick'

# Start:until to the end
In [115]: sentence[4:]
Out[115]: 'quick brown fox jumped over the lazy dog'

# begining:to the end:skip
In [116]: sentence[::2]
Out[116]: 'Teqikbonfxjme vrtelz o'

In [117]: colors[::3]
Out[117]: ['red', 'green']

In [118]: sentence[4:-1:2]
Out[118]: 'qikbonfxjme vrtelz o'

In [119]: colors[1] = "Black"

In [120]: colors
Out[120]: ['red', 'Black', 'yellow', 'green', 'blue', 'purple']

In [121]: colors[2:] = ["Black"] * 4

In [122]: colors
Out[122]: ['red', 'Black', 'Black', 'Black', 'Black', 'Black']

In [123]: sentence[16:19] = "cat"
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-123-a599952598b4> in <module>
----> 1 sentence[16:19] = "cat"

TypeError: 'str' object does not support item assignment

In [124]: sentence[0:16] + "cat" + sentence[19:]
Out[124]: 'The quick brown cat jumped over the lazy dog'

In [124]: sentence[0:16] + "cat" + sentence[19:]
Out[124]: 'The quick brown cat jumped over the lazy dog'

In [125]: sentence.split(' ')
Out[125]: ['The', 'quick', 'brown', 'fox', 'jumped', 'over', 'the', 'lazy', 'dog']

In [126]: "32:45:65".split(:)
  File "<ipython-input-126-a1dd915e1b81>", line 1
    "32:45:65".split(:)
                     ^
SyntaxError: invalid syntax


In [127]: "32:45:65".split(':')
Out[127]: ['32', '45', '65']

In [128]: sentence.split('he')
Out[128]: ['T', ' quick brown fox jumped over t', ' lazy dog']

In [129]: colors
Out[129]: ['red', 'Black', 'Black', 'Black', 'Black', 'Black']

In [130]: colors = ['red', 'orange', 'yellow', 'green', 'blue', 'purple']

In [131]: " - ".join(colors)
Out[131]: 'red - orange - yellow - green - blue - purple'

In [132]: 'red - orange - yellow - green - blue - purple'.split(' - ')
Out[132]: ['red', 'orange', 'yellow', 'green', 'blue', 'purple']
```

Iteration

``` python
In [133]: for color in colors: print("Is " + color + " your favorite")
Is red your favorite
Is orange your favorite
Is yellow your favorite
Is green your favorite
Is blue your favorite
Is purple your favorite

In [135]: for number in [1,2,3,45]:
     ...:     double = number * 2
     ...:     print("Twice " + str(number) + " is " + str(double))
     ...:
Twice 1 is 2
Twice 2 is 4
Twice 3 is 6
Twice 45 is 90

In [136]: modfiers = ["Dark", "Light", "Brownish"]

In [138]: for c in colors:
     ...:     for m in modfiers:
     ...:         print(m + " " + c)
     ...:
     ...:
Dark red
Light red
Brownish red
Dark orange
Light orange
Brownish orange
Dark yellow
Light yellow
Brownish yellow
Dark green
Light green
Brownish green
Dark blue
Light blue
Brownish blue
Dark purple
Light purple
Brownish purple

In [141]: for v in "aeiou":
     ...:     print(v)
     ...:
a
e
i
o
u

In [146]: countdown = 10

In [147]: while countdown >=0:
     ...:     print(str(countdown))
     ...:     countdown -= 1
     ...:
10
9
8
7
6
5
4
3
2
1
0


In [149]: while False:
     ...:     print("OOOps")
     ...:
     ...:

In [150]: name = ["Daniel", "James", "Peter", "Sean"]

In [151]: names = ["Daniel", "James", "Peter", "Sean"]

In [152]: names.pop()
Out[152]: 'Sean'

In [153]: names
Out[153]: ['Daniel', 'James', 'Peter']

In [154]: names.pop()
Out[154]: 'Peter'

In [155]: names.pop()
Out[155]: 'James'

In [156]: names.pop()
Out[156]: 'Daniel'

In [157]: names.pop()
---------------------------------------------------------------------------
IndexError                                Traceback (most recent call last)
<ipython-input-157-15279cb2cf42> in <module>
----> 1 names.pop()

IndexError: pop from empty list

In [160]: while names:
     ...:     print("Welcome, Mr. " + names.pop())
     ...:

In [161]: names = ["Daniel", "James", "Peter", "Sean"]

In [162]: while names:
     ...:     print("Welcome, Mr. " + names.pop())
     ...:
Welcome, Mr. Sean
Welcome, Mr. Peter
Welcome, Mr. James
Welcome, Mr. Daniel

In [163]: names.append("Larry")

In [164]: names.append("Moe")

In [165]: names.append("Homer")

In [166]: while names:
     ...:     print("Welcome, Mr. " + names.pop())
     ...:
Welcome, Mr. Homer
Welcome, Mr. Moe
Welcome, Mr. Larry
```

some built-in functions
``` python
In [2]: abs(-2)
Out[2]: 2

In [3]: bin(143)
Out[3]: '0b10001111'

In [4]: round(3.1)
Out[4]: 3

In [5]: sum([1,2,3])
Out[5]: 6

In [6]: max([ -50, 100, 500, 8])
Out[6]: 500

In [7]: min([ -50, 100, 500, 8])
Out[7]: -50

In [10]: for x in range(5): print(x)
0
1
2
3
4

In [12]: sorted('abracadabra')
Out[12]: ['a', 'a', 'a', 'a', 'a', 'b', 'b', 'c', 'd', 'r', 'r']

In [13]: reversed('abracadabra')
Out[13]: <reversed at 0x1560b2f9b80>

In [14]: reversed(sorted('abracadabra'))
Out[14]: <list_reverseiterator at 0x1560b3689a0>

In [15]: list(reversed(sorted('abracadabra')))
Out[15]: ['r', 'r', 'd', 'c', 'b', 'b', 'a', 'a', 'a', 'a', 'a']

In [16]: ''.join(reversed(sorted('abracadabra')))
Out[16]: 'rrdcbbaaaaa'

In [17]: ''.join(reversed(sorted(["Bob", "Alice", "Charlie", "Aardvark"])))
Out[17]: 'CharlieBobAliceAardvark'

In [18]: print = 5 + 8

In [19]: print("Heelo")
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-19-d29db61a011d> in <module>
----> 1 print("Heelo")

TypeError: 'int' object is not callable

```

Functions in types

``` python
In [1]: 'A long string'.split(' ')
Out[1]: ['A', 'long', 'string']

In [2]: a_string = "Apples, oranges, and bananas"

In [3]: a_string.find('an')
Out[3]: 10

In [4]: a_string[10:]
Out[4]: 'anges, and bananas'

In [5]: "Hello! {0}, welcome to {1}".format("GuD", "Phyton")
Out[5]: 'Hello! GuD, welcome to Phyton'

In [6]: "There are {0} items in your cat.".format(5)
Out[6]: 'There are 5 items in your cat.'

In [9]: a_list = "This is a string".split(" ")

In [10]: a_list.sort()

In [11]: a_list
Out[11]: ['This', 'a', 'is', 'string']

In [12]: a_list.reverse()

In [13]: a_list
Out[13]: ['string', 'is', 'a', 'This']

In [14]: a_list.remove('a')

In [15]: a_list
Out[15]: ['string', 'is', 'This']

In [16]: b_list = a_list

In [17]: b_list.pop()
Out[17]: 'This'

In [18]: a_list
Out[18]: ['string', 'is']

In [19]: c_list = a_list.copy()

In [20]: c_list.append("Owls")

In [21]: c_list
Out[21]: ['string', 'is', 'Owls']

In [22]: a_list
Out[22]: ['string', 'is']

```


custom functions

``` python
In [24]: def noop(): pass

In [25]: noop()

In [26]: def greet(name): print("Hellp, {0}".format(name))

In [27]: greet("GuD")
Hellp, GuD

In [29]: def product(numbers):
    ...:     p = 1
    ...:     for n in numbers:
    ...:         p *= n
    ...:     return p
    ...:

In [30]: product([1,2,3,4])
Out[30]: 24

In [31]: def combine_and_sort(first, second):
    ...:     return sorted((first + second))
    ...:

In [32]: combine_and_sort([1, 3, 5], [2, 4 , 6])
Out[32]: [1, 2, 3, 4, 5, 6]

In [39]: def naughty_product(numbers):
    ...:     p = 1
    ...:     while numbers:
    ...:         p *= numbers.pop()
    ...:     return p
    ...:

In [42]: naughty_product([1,2,3,4])
Out[42]: 24

In [43]: nums = [1, 2, 3, 4]

In [44]: nums
Out[44]: [1, 2, 3, 4]

In [45]: naughty_product(nums)
Out[45]: 24

In [46]: nums
Out[46]: []    

```


roman to decimals
``` python
In [79]: def to_val(letter):
    ...:     letters = "ivxlcm"
    ...:     numbers = [1, 5, 10, 50, 100, 1000]
    ...:     return numbers[letters.find(letter)]
    ...:
    ...:

In [97]: def numerus(roman):
    ...:     total = 0
    ...:     prev = 0
    ...:
    ...:     for l in roman:
    ...:         cur = to_val(l)
    ...:         if (prev < cur):
    ...:             total -= prev
    ...:             cur -= prev
    ...:         total += cur
    ...:         prev = cur
    ...:
    ...:     return total
    ...:
    ...:

In [98]: numerus("xiv")
Out[98]: 14

In [99]: numerus("mmciv")
Out[99]: 2104

In [100]: numerus("mmxlix")
Out[100]: 2049

```

None

``` python
In [106]: None

In [107]: my_data = ""

In [108]: if my_data: print("Got data?")

In [109]: my_data = False

In [110]: if my_data: print("Got data?")

In [111]: my_data = None

In [112]: if my_data: print("Got data?")

In [113]: mydata = True

In [114]: if my_data: print("Got data?")

In [115]: my_data = "Yes"

In [116]: if my_data: print("Got data?")
Got data?

In [118]: if my_data is None:
     ...:     print("Not set")
     ...:

In [119]: my_data = None

In [120]: if my_data is None:
     ...:     print("Not set")
     ...:
Not set

In [121]: my_data = ""

In [122]: if my_data is None:
     ...:     print("Not set")
     ...:

In [123]: my_date = 0

In [124]: if my_data is None:
     ...:     print("Not set")
     ...:

In [125]: my_date = False

In [126]: if my_data is None:
     ...:     print("Not set")
     ...:

```

Dictionaries NOT ordered can´t assume items will be in the same order as put

``` python
In [127]: cats = {}

In [128]: cats["GuD"] = 5

In [129]: cats["Robin"] = 2

In [130]: cats["Alice"] = 9

In [131]: cats
Out[131]: {'GuD': 5, 'Robin': 2, 'Alice': 9}

In [132]: cats["Alice"] = 20

In [133]: cats["CatWoman"] = 20

In [134]: cats
Out[134]: {'GuD': 5, 'Robin': 2, 'Alice': 20, 'CatWoman': 20}

In [135]: cats["alice"] = 8

In [136]: cats
Out[136]: {'GuD': 5, 'Robin': 2, 'Alice': 20, 'CatWoman': 20, 'alice': 8}

In [137]: cats["GuD"]
Out[137]: 5

In [138]: cats["Caty"]
---------------------------------------------------------------------------
KeyError                                  Traceback (most recent call last)
<ipython-input-138-0cbcfa1cf363> in <module>
----> 1 cats["Caty"]

KeyError: 'Caty'

In [140]: cats.get("Caty")

In [141]: cats.get("Caty",None)

In [142]: cats.get("Caty", 0)
Out[142]: 0

In [144]: "GuD" in cats
Out[144]: True

In [145]: "GuDi" in cats
Out[145]: False

In [146]: {'GuD': 5, 'Robin': 2, 'Alice': 9}
Out[146]: {'GuD': 5, 'Robin': 2, 'Alice': 9}

In [147]: for name in cats: print(name)
GuD
Robin
Alice
CatWoman
alice

In [148]: for name in cats: print("{0} has {1} cat(s)".format(name, cats[name]))
GuD has 5 cat(s)
Robin has 2 cat(s)
Alice has 20 cat(s)
CatWoman has 20 cat(s)
alice has 8 cat(s)

In [149]: for name in cats.keys(): print("{0} has {1} cat(s)".format(name, cats[name]))
GuD has 5 cat(s)
Robin has 2 cat(s)
Alice has 20 cat(s)
CatWoman has 20 cat(s)
alice has 8 cat(s)

In [152]: for num_cats in cats.values(): print("someone has {0} cat(s)".format(num_cats))
someone has 5 cat(s)
someone has 2 cat(s)
someone has 20 cat(s)
someone has 20 cat(s)
someone has 8 cat(s)

In [153]: for (person, num_cates) in cats.items(): print("{1} has {0} cat(s)".format(person, num_cates))
5 has GuD cat(s)
2 has Robin cat(s)
20 has Alice cat(s)
20 has CatWoman cat(s)
8 has alice cat(s)

In [154]: del cats["Alice"]

In [155]: for (person, num_cates) in cats.items(): print("{1} has {0} cat(s)".format(person, num_cates))
5 has GuD cat(s)
2 has Robin cat(s)
20 has CatWoman cat(s)
8 has alice cat(s)

In [156]: cats.pop("alice")
Out[156]: 8

In [157]: cats
Out[157]: {'GuD': 5, 'Robin': 2, 'CatWoman': 20}

In [159]: cats.pop("alice")
---------------------------------------------------------------------------
KeyError                                  Traceback (most recent call last)
<ipython-input-159-daa4c8fbcb22> in <module>
----> 1 cats.pop("alice")

KeyError: 'alice'

In [160]: cats.pop("alice", 0)
Out[160]: 0

In [162]: users = { 1: { "name": "Joe", "email": "joe@example.com"}, 2: {"name": "Sarah", "email": "sarah@example.com"} }

In [163]: users
Out[163]:
{1: {'name': 'Joe', 'email': 'joe@example.com'},
 2: {'name': 'Sarah', 'email': 'sarah@example.com'}}

In [164]:
```


Binary Data

``` python
n [164]: b = bytes()

In [165]: b
Out[165]: b''

In [169]: greeting = b"Hello, world!"

In [170]: print(greeting)
b'Hello, world!'

In [172]: for c in greeting: print(c)
72
101
108
108
111
44
32
119
111
114
108
100
33

In [173]: greeting[0] = 80
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-173-78db58199e16> in <module>
----> 1 greeting[0] = 80

TypeError: 'bytes' object does not support item assignment

In [174]: ba = bytearray()

In [175]: data = bytearray()

In [176]: data
Out[176]: bytearray(b'')

In [177]: data += b"HI, how are yhou"

In [178]: data
Out[178]: bytearray(b'HI, how are yhou')

In [179]: data[0] = 120

In [180]: data
Out[180]: bytearray(b'xI, how are yhou')
```

tuples, imutable, like lists but better perform

``` python
In [183]: fruits = ("Apple", "Orange", "lemon")

In [184]: fruits
Out[184]: ('Apple', 'Orange', 'lemon')

In [185]: fruits[0]
Out[185]: 'Apple'

In [186]: fruits.append("Straeberry")
---------------------------------------------------------------------------
AttributeError                            Traceback (most recent call last)
<ipython-input-186-b25df12635ad> in <module>
----> 1 fruits.append("Straeberry")

AttributeError: 'tuple' object has no attribute 'append'

In [187]: fruits[0] = "Strawberry"
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-187-05c661ca2e13> in <module>
----> 1 fruits[0] = "Strawberry"

TypeError: 'tuple' object does not support item assignment

In [188]: list(fruits)
Out[188]: ['Apple', 'Orange', 'lemon']

In [189]: tuple(list(fruits))
Out[189]: ('Apple', 'Orange', 'lemon')

In [190]:

In [190]: red = (255, 0,0)

In [191]: purple = (255, 0, 255)

In [194]: grades = ([95, 90], [50, 90])

In [195]: grades[1]
Out[195]: [50, 90]

In [196]: grades[1] = [100, 100]
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-196-1c4bea8cb0e6> in <module>
----> 1 grades[1] = [100, 100]

TypeError: 'tuple' object does not support item assignment

In [197]: grades[1][0] = [100]

In [198]: grades
Out[198]: ([95, 90], [[100], 90])
```

Sets

```` python
In [200]: vegetables = {"aspargus", "onion", "Carrot", "tomato"}

In [201]: vegetable[0]
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-201-bcc19d01eb14> in <module>
----> 1 vegetable[0]

NameError: name 'vegetable' is not defined

In [202]: for v in vegetables: print(v)
tomato
onion
aspargus
Carrot

In [204]: vegetables.pop()
Out[204]: 'tomato'

In [205]: vegetables
Out[205]: {'Carrot', 'aspargus', 'onion'}

In [208]: vegetables.remove("onion")

In [209]: vegetables
Out[209]: {'Carrot', 'aspargus'}

In [210]: vegetables.add("radish")

In [211]: vegetables
Out[211]: {'Carrot', 'aspargus', 'radish'}

In [212]: vegetables.add("radish")

In [213]: vegetables
Out[213]: {'Carrot', 'aspargus', 'radish'}

In [214]: vegetables.add("radish")

In [215]: vegetables
Out[215]: {'Carrot', 'aspargus', 'radish'}

In [216]: vegetables = {"aspargus", "onion", "Carrot", "tomato"}

````

operations between objects
```` python
In [224]: fruits
Out[224]: ('Apple', 'Orange', 'lemon', 'tomato')

In [225]: vegetables
Out[225]: {'Carrot', 'aspargus', 'onion', 'tomato'}

In [228]: vegetables.intersection(fruits)
Out[228]: {'tomato'}

In [229]: set(fruits)
Out[229]: {'Apple', 'Orange', 'lemon', 'tomato'}

In [230]: list(set(tuple(vegetables)))
Out[230]: ['tomato', 'onion', 'aspargus', 'Carrot']
````

frozen set
```` python
In [235]: frozen = frozenset(vegetables)

In [236]: frozen.pop()
---------------------------------------------------------------------------
AttributeError                            Traceback (most recent call last)
<ipython-input-236-e5998602b592> in <module>
----> 1 frozen.pop()

AttributeError: 'frozenset' object has no attribute 'pop'

````

other list functions
```` python
In [238]: colors = { "Red": (255, 0, 0, 0), "Yellow": (255, 255, 0), "Purple": (255, 0, 255) }

In [241]: for (name, rgb) in colors.items(): print("{0} is {1}".format(name, rgb))
Red is (255, 0, 0, 0)
Yellow is (255, 255, 0)
Purple is (255, 0, 255)

In [242]: for (i, c) in enumerate(fruits): print(i,c)
0 Apple
1 Orange
2 lemon
3 tomato

In [243]: for (f, v) in zip(fruits, vegetables): print(f,v)
Apple tomato
Orange onion
lemon aspargus
tomato Carrot

In [244]: fruits
Out[244]: ('Apple', 'Orange', 'lemon', 'tomato')

In [245]: vegetables
Out[245]: {'Carrot', 'aspargus', 'onion', 'tomato'}

In [246]: vegetables.add("Rhubard")

In [247]: for (f, v) in zip(fruits, vegetables): print(f,v)
Apple Rhubard
Orange onion
lemon Carrot
tomato tomato
````

continue break else

```` python
In [252]: haystack = ["Hey" ] * 20

In [253]: haystack[6] = "needle"

In [254]: haystack
Out[254]:
['Hey',
 'Hey',
 'Hey',
 'Hey',
 'Hey',
 'Hey',
 'needle',
 'Hey',
 'Hey',
 'Hey',
 'Hey',
 'Hey',
 'Hey',
 'Hey',
 'Hey',
 'Hey',
 'Hey',
 'Hey',
 'Hey',
 'Hey']

 In [257]: for (i, v) in enumerate(haystack):
     ...:     print("Looking...", i)
     ...:     if v == "needle":
     ...:         idx = i
     ...:         print("Found id!", idx)
     ...:
Looking... 0
Looking... 1
Looking... 2
Looking... 3
Looking... 4
Looking... 5
Looking... 6
Found id! 6
Looking... 7
Looking... 8
Looking... 9
Looking... 10
Looking... 11
Looking... 12
Looking... 13
Looking... 14
Looking... 15
Looking... 16
Looking... 17
Looking... 18
Looking... 19

In [258]: haystack[idx]
Out[258]: 'needle'

In [260]: idx
Out[260]: 6

In [261]: for (i, v) in enumerate(haystack):
     ...:     print("Looking...", i)
     ...:     if v == "needle":
     ...:         idx = i
     ...:         print("Found id!", idx)
     ...:         break
     ...:
Looking... 0
Looking... 1
Looking... 2
Looking... 3
Looking... 4
Looking... 5
Looking... 6
Found id! 6

In [265]: for (i, v) in enumerate(haystack):
     ...:     print("Looking...", i)
     ...:     if v == "Hey":
     ...:         continue
     ...:     idx = i
     ...:     print("Found id!", idx)
     ...:     break
     ...:
Looking... 0
Looking... 1
Looking... 2
Looking... 3
Looking... 4
Looking... 5
Looking... 6
Found id! 6
In [266]: for (i, v) in enumerate(haystack):
     ...:     print("Looking...", i)
     ...:     if v == "Hey":
     ...:         continue
     ...:     idx = i
     ...:     print("Found id!", idx)
     ...:     break
     ...: else:
     ...:     print("Coulnd~t findit")
     ...:
Looking... 0
Looking... 1
Looking... 2
Looking... 3
Looking... 4
Looking... 5
Looking... 6
Found id! 6

In [267]: haystack = ["Hey") * 20
  File "<ipython-input-267-0609cb55b1e7>", line 1
    haystack = ["Hey") * 20
                     ^
SyntaxError: closing parenthesis ')' does not match opening parenthesis '['


In [268]: haystack = ["Hey"] * 20

In [269]: for (i, v) in enumerate(haystack):
     ...:     print("Looking...", i)
     ...:     if v == "Hey":
     ...:         continue
     ...:     idx = i
     ...:     print("Found id!", idx)
     ...:     break
     ...: else:
     ...:     print("Coulnd~t findit")
     ...:
Looking... 0
Looking... 1
Looking... 2
Looking... 3
Looking... 4
Looking... 5
Looking... 6
Looking... 7
Looking... 8
Looking... 9
Looking... 10
Looking... 11
Looking... 12
Looking... 13
Looking... 14
Looking... 15
Looking... 16
Looking... 17
Looking... 18
Looking... 19
Coulnd~t findit
````

list comprehenssion

```` python
In [271]: for i in range(1, 21):
     ...:     print(i)
     ...:
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20

In [272]: powers = []

In [273]: for i in range(1, 21):
     ...:     powers.append(2 ** i)
     ...:

In [274]: powers
Out[274]:
[2,
 4,
 8,
 16,
 32,
 64,
 128,
 256,
 512,
 1024,
 2048,
 4096,
 8192,
 16384,
 32768,
 65536,
 131072,
 262144,
 524288,
 1048576]

In [275]: powers = [2 ** i for i in range(1, 21)]

In [276]: powers
Out[276]:
[2,
 4,
 8,
 16,
 32,
 64,
 128,
 256,
 512,
 1024,
 2048,
 4096,
 8192,
 16384,
 32768,
 65536,
 131072,
 262144,
 524288,
 1048576]
````

input and errors
```` python
In [278]: input()
Hello
Out[278]: 'Hello'

In [279]: name = input()
GuD

In [281]: name
Out[281]: 'GuD'

In [282]: name = input("Name?")
Name? GuD

In [283]: age_str = input("Age: ")
Age: 41

In [284]: age = int(age_str)

In [285]: age
Out[285]: 41

In [286]: age_str
Out[286]: '41'

In [287]: age = int(input("Age: "))
Age: five
---------------------------------------------------------------------------
ValueError                                Traceback (most recent call last)
<ipython-input-287-b84953505461> in <module>
----> 1 age = int(input("Age: "))

ValueError: invalid literal for int() with base 10: 'five'

In [288]: while True:
     ...:     num = input("Enter a numer: ")
     ...:     if not num: break
     ...:
Enter a numer: 4
Enter a numer: 5
Enter a numer: 2
Enter a numer: a
Enter a numer: zero
Enter a numer:

In [290]: total = 0

In [291]: while True:
     ...:     num = input("Enter a numer: ")
     ...:     if not num: break
     ...:     total += int(num)
     ...:     print("Total: " + str(total))
     ...:
     ...:
Enter a numer: 5
Total: 5
Enter a numer:

In [292]: while True:
     ...:     num = input("Enter a numer: ")
     ...:     if not num: break
     ...:     total += int(num)
     ...:     print("Total: " + str(total))
     ...:
     ...:
Enter a numer: 4
Total: 9
Enter a numer: 5
Total: 14
Enter a numer: 2
Total: 16
Enter a numer:

In [293]: while True:
     ...:     num = input("Enter a numer: ")
     ...:     if not num: break
     ...:     total += int(num)
     ...:     print("Total: " + str(total))
     ...:
     ...:
Enter a numer: f
---------------------------------------------------------------------------
ValueError                                Traceback (most recent call last)
<ipython-input-293-384df05cace7> in <module>
      2     num = input("Enter a numer: ")
      3     if not num: break
----> 4     total += int(num)
      5     print("Total: " + str(total))
      6

ValueError: invalid literal for int() with base 10: 'f'

In [294]: "5".isdigit()
Out[294]: True

In [295]: "51212".isdigit()
Out[295]: True

In [296]: num_inp = input("Enter a numer: ")
Enter a numer: 4

In [297]: if not num_inp.isdigit():
     ...:     print("Fine, be that way")
     ...:

In [299]: num_inp = input("Enter a numer: ")
Enter a numer: f

In [300]: if not num_inp.isdigit():
     ...:     print("Fine, be that way")
     ...:
Fine, be that way

In [302]: if not num_inp.isdigit():
     ...:     print("Fine, be that way")
     ...: else:
     ...:     product = int(num_inp) * 7
     ...:     print("{0} times seven {1}".format(num_inp, product))
     ...:
     ...:
Fine, be that way

In [303]: num_inp = input("Enter a numer: ")
Enter a numer: 4

In [304]: if not num_inp.isdigit():
     ...:     print("Fine, be that way")
     ...: else:
     ...:     product = int(num_inp) * 7
     ...:     print("{0} times seven {1}".format(num_inp, product))
     ...:
     ...:
4 times seven 28

In [305]:
````

error handling

```` python
In [306]: int(" 5 ")
Out[306]: 5

In [307]: " 5 ".isdigit()
Out[307]: False

In [308]: int("-55")
Out[308]: -55

In [309]: "-55".isdigit()
Out[309]: False

In [310]: while True:
     ...:     try:
     ...:         inp = input("Enter a number: ")
     ...:         inp_int = int(inp)
     ...:         break
     ...:     except:
     ...:         inp_int = None
     ...:         print("Not a number")
     ...:
Enter a number: d
Not a number
Enter a number: f
Not a number
Enter a number: 3

In [7]: try:
   ...:     inp = TYPOinput("Enter a number: ")
   ...:     inp_int = int(inp)
   ...: except:
   ...:     inp_int = None
   ...:     print("Not a number")
   ...:
Not a number

In [8]: try:
   ...:     inp = input("Enter a number: ")
   ...:     inp_int = int(inp)
   ...: except:
   ...:     inp_int = None
   ...:     print("Not a number")
   ...:
Enter a number: a
Not a number

In [11]:  inp = int(input("Enter a number: "))
Enter a number: a
---------------------------------------------------------------------------
ValueError                                Traceback (most recent call last)
<ipython-input-11-f0afb09b6b0a> in <module>
----> 1 inp = int(input("Enter a number: "))

ValueError: invalid literal for int() with base 10: 'a'

In [12]: try:
    ...:     inp = TYPOinput("Enter a number: ")
    ...:     inp_int = int(inp)
    ...: except ValueError:
    ...:     inp_int = None
    ...:     print("Not a number")
    ...:
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-12-b378cd6411e4> in <module>
      1 try:
----> 2     inp = TYPOinput("Enter a number: ")
      3     inp_int = int(inp)
      4 except ValueError:
      5     inp_int = None

NameError: name 'TYPOinput' is not defined

In [13]: try:
    ...:     inp = input("Enter a number: ")
    ...:     inp_int = int(inp)
    ...: except ValueError:
    ...:     inp_int = None
    ...:     print("Not a number")
    ...:
Enter a number: a
Not a number

In [14]: try:
    ...:     inp = input("Enter a number: ")
    ...:     inp_int = int(inp)
    ...: except ValueError:
    ...:     inp_int = None
    ...:     print("Not a number")
    ...: except NameError:
    ...:     print("Something wrong in the code")
    ...: except:
    ...:     print("Someting else went wrong")
    ...:
Enter a number: Someting else went wrong

KeyboardInterrupt escaped interact()

In [16]: try:
    ...:     inp = iput("Enter a number: ")
    ...:     inp_int = int(inp)
    ...: except ValueError:
    ...:     inp_int = None
    ...:     print("Not a number")
    ...: except NameError as e:
    ...:     print("Something wrong in the code")
    ...:     print(e)
    ...: except:
    ...:     print("Someting else went wrong")
    ...:
Something wrong in the code
name 'iput' is not defined

In [17]: try:
    ...:     inp = input("Enter a number: ")
    ...:     inp_int = int(inp)
    ...: except ValueError:
    ...:     inp_int = None
    ...:     print("Not a number")
    ...: except NameError as e:
    ...:     print("Something wrong in the code")
    ...:     print(e)
    ...: except:
    ...:     print("Someting else went wrong")
    ...:
Enter a number:
Not a number

In [18]: try:
    ...:     inp = iput("Enter a number: ")
    ...:     inp_int = int(inp)
    ...: except ValueError:
    ...:     inp_int = None
    ...:     print("Not a number")
    ...: except NameError as e:
    ...:     print("Something wrong in the code")
    ...:     print(e)
    ...:     raise(e)
    ...: except:
    ...:     print("Someting else went wrong")
    ...:
Something wrong in the code
name 'iput' is not defined
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-18-f7fc5c5f3544> in <module>
      8     print("Something wrong in the code")
      9     print(e)
---> 10     raise(e)
     11 except:
     12     print("Someting else went wrong")

<ipython-input-18-f7fc5c5f3544> in <module>
      1 try:
----> 2     inp = iput("Enter a number: ")
      3     inp_int = int(inp)
      4 except ValueError:
      5     inp_int = None

NameError: name 'iput' is not defined

In [19]: try:
    ...:     inp = input("Enter a number: ")
    ...:     inp_int = int(inp)
    ...: except ValueError:
    ...:     inp_int = None
    ...:     print("Not a number")
    ...: except NameError as e:
    ...:     print("Something wrong in the code")
    ...:     print(e)
    ...:     raise(e)
    ...: except:
    ...:     print("Someting else went wrong")
    ...:
Enter a number: 2

In [20]: try:
    ...:     inp = iput("Enter a number: ")
    ...:     inp_int = int(inp)
    ...: except ValueError:
    ...:     inp_int = None
    ...:     print("Not a number")
    ...: except NameError as e:
    ...:     print("Something wrong in the code")
    ...:     print(e)
    ...:     raise(e)
    ...: except:
    ...:     print("Someting else went wrong")
    ...: finally:
    ...:     print("all done")
    ...:
Something wrong in the code
name 'iput' is not defined
all done
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-20-dabc77d66498> in <module>
      8     print("Something wrong in the code")
      9     print(e)
---> 10     raise(e)
     11 except:
     12     print("Someting else went wrong")

<ipython-input-20-dabc77d66498> in <module>
      1 try:
----> 2     inp = iput("Enter a number: ")
      3     inp_int = int(inp)
      4 except ValueError:
      5     inp_int = None

NameError: name 'iput' is not defined

In [21]: try:
    ...:     inp = input("Enter a number: ")
    ...:     inp_int = int(inp)
    ...: except ValueError:
    ...:     inp_int = None
    ...:     print("Not a number")
    ...: except NameError as e:
    ...:     print("Something wrong in the code")
    ...:     print(e)
    ...:     raise(e)
    ...: except:
    ...:     print("Someting else went wrong")
    ...: finally:
    ...:     print("all done")
    ...:
Enter a number: 4
all done

In [22]: name
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-22-9bc0cb2ed6de> in <module>
----> 1 name

NameError: name 'name' is not defined

In [23]: name = input("Name? ")
Name? GuD

In [24]: if name[0] == "G": raise ValueError("A G!")
---------------------------------------------------------------------------
ValueError                                Traceback (most recent call last)
<ipython-input-24-c4f9a7dbc9ef> in <module>
----> 1 if name[0] == "G": raise ValueError("A G!")

ValueError: A G!

In [26]: try:
    ...:     inp = iput("Enter a number: ")
    ...:     inp_int = int(inp)
    ...: except ValueError:
    ...:     inp_int = None
    ...:     print("Not a number")
    ...: except NameError as e:
    ...:     print("Something wrong in the code")
    ...:     print(e)
    ...:     raise(e)
    ...: except:
    ...:     print("Someting else went wrong")
    ...: else:
    ...:     print("All OK")
    ...: finally:
    ...:     print("all done")
    ...:
Something wrong in the code
name 'iput' is not defined
all done
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-26-309580e5a37f> in <module>
      8     print("Something wrong in the code")
      9     print(e)
---> 10     raise(e)
     11 except:
     12     print("Someting else went wrong")

<ipython-input-26-309580e5a37f> in <module>
      1 try:
----> 2     inp = iput("Enter a number: ")
      3     inp_int = int(inp)
      4 except ValueError:
      5     inp_int = None

NameError: name 'iput' is not defined

In [27]: try:
    ...:     inp = input("Enter a number: ")
    ...:     inp_int = int(inp)
    ...: except ValueError:
    ...:     inp_int = None
    ...:     print("Not a number")
    ...: except NameError as e:
    ...:     print("Something wrong in the code")
    ...:     print(e)
    ...:     raise(e)
    ...: except:
    ...:     print("Someting else went wrong")
    ...: else:
    ...:     print("All OK")
    ...: finally:
    ...:     print("all done")
    ...:
Enter a number: 3
All OK
all done

````

access files

with -> Context delimmiter, used with open, closes the file when with block ends

```` python
In [2]: with open("recipe.txt") as input_file:
   ...:     recipe = input_file.read()
   ...:

In [3]: print(recipe)
Spaghetti Recipe

1 Spaghetti
1 Sauce

Cook the spaghetti. Add the sauce. Serve.


In [4]: with open("words.txt") as input_file:
   ...:     for line in input_file:
   ...:         if line[0] == 'x': print(line)
   ...:
x

xanthaline

xanthamic

In [6]: word = "a word\n"

In [7]: print(word)
a word


In [8]: print(word.strip())
a word

In [9]: print(word)
a word


In [11]: " How are you".strip()
Out[11]: 'How are you'

In [12]: with open("words.txt") as input_file:
    ...:     for line in input_file:
    ...:         line = line.strip()
    ...:         if len(line) < 4: continue
    ...:         if line[0] == 'x' and line [3] == 'y': print(line)
    ...:
    ...:
xenyl
xenylamine
xylyl
xylylene
xylylic

In [15]: words = []

In [17]: with open("words.txt") as input_file:
    ...:     for line in input_file:
    ...:         line = line.strip()
    ...:         if len(line) < 4: continue
    ...:         if line[0] == 'x' and line [3] == 'y': words.append(line)
    ...:
    ...:
    ...:

In [18]: words
Out[18]: ['xenyl', 'xenylamine', 'xylyl', 'xylylene', 'xylylic']

# w always overwrite file
In [24]: with open('scrabble.txt', 'w') as output_file:
    ...:     for word in words:
    ...:         output_file.write(word + "\n")
    ...:

In [26]: words = []

In [27]: with open("words.txt") as input_file:
    ...:     for line in input_file:
    ...:         line = line.strip()
    ...:         if len(line) < 4: continue
    ...:         if line[0] == 'd' and line [3] == 'o': words.append(line)
    ...:

In [28]:

In [28]: words
Out[28]:
['daboia',
 'daboya',
 'dacoit',
 'dacoitage',
 'dacoity',
 'dado',
 'dagoba',
 'dahoon',

#a appends
In [30]: words = ["alligator", "armadillo"]

In [31]: with open('scrabble.txt', 'a') as output_file:
    ...:     for word in words:
    ...:         output_file.write(word + "\n")
    ...:

# b for binary
n [41]: with open('guru-portfolio.zip', 'rb') as input_file:
    ...:     data = input_file.read()
    ...:

In [42]: type(data)
Out[42]: bytes

In [43]: with open('other.zip', 'wb') as output_file:
    ...:     output_file.write(data)
    ...:
    ...:

In [44]: with open('nemo.txt') as no_file:
    ...:     for line in no_file:
    ...:         print(line)
    ...:
    ...:
---------------------------------------------------------------------------
FileNotFoundError                         Traceback (most recent call last)
<ipython-input-44-fc0e99cb03fa> in <module>
----> 1 with open('nemo.txt') as no_file:
      2     for line in no_file:
      3         print(line)
      4
      5

FileNotFoundError: [Errno 2] No such file or directory: 'nemo.txt'

````

import modules math

```` python
In [47]: import math

In [48]: math.pi
Out[48]: 3.141592653589793

In [49]: math.e
Out[49]: 2.718281828459045

In [50]: math.cos(math.pi)
Out[50]: -1.0

In [51]: math.log(math.e)
Out[51]: 1.0

In [52]: math.floor(-15.4)
Out[52]: -16

In [53]: math.ceil(-15.4)
Out[53]: -15
````

import modules random
```` python
In [54]: import random

In [55]: random.random()
Out[55]: 0.5298348878622277

In [56]: random.random()
Out[56]: 0.9844217923668475

In [57]: random.random()
Out[57]: 0.2225549771488693

In [58]: random.randint(3,18)
Out[58]: 17

In [59]: random.randint(3,18)
Out[59]: 15

In [60]: random.randint(3,18)
Out[60]: 14

In [61]: random.choice(['Happy', "Dopey", "Doc", "Grumpy"])
Out[61]: 'Grumpy'

In [62]: random.choice(['Happy', "Dopey", "Doc", "Grumpy"])
Out[62]: 'Grumpy'

In [63]: random.choice(['Happy', "Dopey", "Doc", "Grumpy"])
Out[63]: 'Grumpy'

In [64]: random.choice(['Happy', "Dopey", "Doc", "Grumpy"])
Out[64]: 'Dopey'

In [65]: random.choice("aeiou")
Out[65]: 'e'

In [66]: random.choice("aeiou")
Out[66]: 'a'

In [67]: suits = ('hearts', 'diamonds', 'clubs', 'spades')

In [71]: values = range(1, 14)

In [72]: list(values)
Out[72]: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13]

In [76]: cards = []

In [77]: for s in suits:
    ...:     for v in values:
    ...:         cards.append("{0} of {1}".format(v, s))
    ...:

In [78]: cards
Out[78]:
['1 of hearts',
 '2 of hearts',
 '3 of hearts',
 '4 of hearts',
 '5 of hearts',
 '6 of hearts',
 '7 of hearts',
 '8 of hearts',
 '9 of hearts',
 '10 of hearts',
 '11 of hearts',
 '12 of hearts',
 '13 of hearts',
 '1 of diamonds',
 '2 of diamonds',
 '3 of diamonds',
 '4 of diamonds',
 '5 of diamonds',
 '6 of diamonds',
 '7 of diamonds',
 '8 of diamonds',
 '9 of diamonds',
 '10 of diamonds',
 '11 of diamonds',
 '12 of diamonds',
 '13 of diamonds',
 '1 of clubs',
 '2 of clubs',
 '3 of clubs',
 '4 of clubs',
 '5 of clubs',
 '6 of clubs',
 '7 of clubs',
 '8 of clubs',
 '9 of clubs',
 '10 of clubs',
 '11 of clubs',
 '12 of clubs',
 '13 of clubs',
 '1 of spades',
 '2 of spades',
 '3 of spades',
 '4 of spades',
 '5 of spades',
 '6 of spades',
 '7 of spades',
 '8 of spades',
 '9 of spades',
 '10 of spades',
 '11 of spades',
 '12 of spades',
 '13 of spades']

In [79]: random.choice(cards)
Out[79]: '3 of hearts'

In [80]: random.choice(cards)
Out[80]: '2 of clubs'

In [81]: random.shuffle(cards)

In [82]: cards
Out[82]:
['9 of hearts',
 '12 of spades',
 '10 of spades',
 '10 of hearts',
 '7 of spades',
 '12 of hearts',
 '5 of clubs',
 '7 of hearts',
 '12 of diamonds',
 '1 of diamonds',
 '10 of clubs',
 '1 of hearts',
 '11 of hearts',
 '13 of diamonds',
 '8 of spades',
 '11 of clubs',
 '3 of clubs',
 '1 of spades',
 '2 of spades',
 '9 of spades',
 '6 of spades',
 '2 of clubs',
 '8 of hearts',
 '1 of clubs',
 '5 of spades',
 '4 of diamonds',
 '11 of diamonds',
 '6 of diamonds',
 '7 of diamonds',
 '11 of spades',
 '5 of diamonds',
 '6 of clubs',
 '3 of spades',
 '3 of diamonds',
 '6 of hearts',
 '10 of diamonds',
 '4 of clubs',
 '4 of hearts',
 '13 of clubs',
 '2 of diamonds',
 '8 of clubs',
 '9 of clubs',
 '8 of diamonds',
 '7 of clubs',
 '13 of spades',
 '4 of spades',
 '13 of hearts',
 '9 of diamonds',
 '3 of hearts',
 '2 of hearts',
 '5 of hearts',
 '12 of clubs']

````

import only a function
```` python
In [84]: from random import shuffle

In [85]: shuffle(cards)

````

iter tools
```` python
In [88]: import itertools as iter

In [89]: for num in iter.chain([1,2,3],[4,5,6]):
    ...:     print(num)
    ...:
1
2
3
4
5
6

In [92]: for (a, b, c) in iter.combinations(("Peanut butter", "Jelly", "Mayo", "ketchup", "lettuce"),3)
    ...: :
    ...:     print("How about a nice {0}, {1}, and {2} sandwich?".format(a,b,c))
    ...:
How about a nice Peanut butter, Jelly, and Mayo sandwich?
How about a nice Peanut butter, Jelly, and ketchup sandwich?
How about a nice Peanut butter, Jelly, and lettuce sandwich?
How about a nice Peanut butter, Mayo, and ketchup sandwich?
How about a nice Peanut butter, Mayo, and lettuce sandwich?
How about a nice Peanut butter, ketchup, and lettuce sandwich?
How about a nice Jelly, Mayo, and ketchup sandwich?
How about a nice Jelly, Mayo, and lettuce sandwich?
How about a nice Jelly, ketchup, and lettuce sandwich?
How about a nice Mayo, ketchup, and lettuce sandwich?

In [93]:

````

time

```` python
In [94]: import time

In [95]: time.localtime()
Out[95]: time.struct_time(tm_year=2020, tm_mon=10, tm_mday=20, tm_hour=19, tm_min=10, tm_sec=13, tm_wday=1, tm_yday=294, tm_isdst=0)

In [96]: time.gmtime()
Out[96]: time.struct_time(tm_year=2020, tm_mon=10, tm_mday=20, tm_hour=22, tm_min=10, tm_sec=20, tm_wday=1, tm_yday=294, tm_isdst=0)

In [97]: now = time.strftime("%H:%M:%S %p - %A, %B %d %Y", time.gmtime())

In [98]: now
Out[98]: '22:11:33 PM - Tuesday, October 20 2020'

In [99]: time.sleep(5)

In [100]: time.time()
Out[100]: 1603231933.3264282
````

datetime
```` python
In [102]: import datetime

In [103]: now
Out[103]: '22:11:33 PM - Tuesday, October 20 2020'

In [104]: datetime.datetime.strptime(now, "%H:%M:%S %p - %A, %B %d %Y")
Out[104]: datetime.datetime(2020, 10, 20, 22, 11, 33)

In [105]: from datetime import datetime

In [106]: datetime.strptime(now, "%H:%M:%S %p - %A, %B %d %Y")
Out[106]: datetime.datetime(2020, 10, 20, 22, 11, 33)

In [107]:

````

```` python
In [108]: import time

In [109]: time
Out[109]: <module 'time' (built-in)>

In [110]: from datetime import time

In [111]: time
Out[111]: datetime.time

In [112]: now = datetime.now()

In [113]: later = datetime.now()

In [114]: later - now
Out[114]: datetime.timedelta(seconds=7, microseconds=750019)

In [115]: later > now
Out[115]: True
````

zip tools
```` python
In [117]: import gzip

In [118]: import bz2

In [120]: import zipfile

In [121]: from zipfile import ZipFile

In [122]: with ZipFile('files.zip') as files:
     ...:     print(files.namelist())
     ...:
['recipe.txt', 'scrabble.txt']


In [124]: with ZipFile('files.zip') as files:
     ...:     print(files.namelist())
     ...:     files.extractall()
     ...:
['recipe.txt', 'scrabble.txt']

In [125]: dir
Out[125]: <function dir>

In [126]: ls
20/10/2020  19:21                65 Recipe.txt
20/10/2020  19:21                40 scrabble.txt

````

csv
```` python
In [128]: import csv

In [129]: with open('users.csv', 'w') as csvfile:
     ...:     writer = csv.writer(csvfile)
     ...:     writer.writerow(['id', 'email', 'name'])
     ...:     writer.writerow([5, 'robin@exemple.com', 'Robin Norwood'])
     ...:     writer.writerow([6, 'fonzie@example.com', 'Arthur Fonarelli, AKA "The Fonz"'])
     ...:

In [133]: with open("users.csv") as input_file:
     ...:     users = input_file.read()
     ...:

In [135]: print(users)
id,email,name

5,robin@exemple.com,Robin Norwood

6,fonzie@example.com,"Arthur Fonarelli, AKA ""The Fonz"""

````

OS

```` python
In [139]: import os

In [140]: os.getenv('USER')

In [141]: os.getenv('PATH')
Out[141]: 'C:\\Python39\\Scripts\\;C:\\Python39\\;C:\\Program Files\\Java\\jdk1.8.0_201\\bin;C:\\Program Files (x86)\\Common Files\\Oracle\\Java\\javapath;C:\\WINDOWS\\system32;C:\\WINDOWS;C:\\WINDOWS\\System32\\Wbem;C:\\WINDOWS\\System32\\WindowsPowerShell\\v1.0\\;C:\\WINDOWS\\System32\\OpenSSH\\;C:\\Program Files\\Microsoft VS Code\\bin;C:\\Program Files\\k6\\;C:\\Program Files\\Intel\\WiFi\\bin\\;C:\\Program Files\\Common Files\\Intel\\WirelessCommon\\;C:\\Program Files (x86)\\Intel\\Intel(R) Management Engine Components\\DAL;C:\\Program Files\\Intel\\Intel(R) Management Engine Components\\DAL;C:\\Program Files (x86)\\Yarn\\bin\\;C:\\Program Files\\Git\\cmd;C:\\Program Files\\Amazon\\AWSSAMCLI\\bin\\;C:\\oracle\\nodejs\\;C:\\Program Files\\Docker\\Docker\\resources\\bin;C:\\ProgramData\\DockerDesktop\\version-bin;C:\\Program Files\\PuTTY\\;C:\\Program Files\\Amazon\\AWSCLIV2\\;C:\\ProgramData\\chocolatey\\bin;C:\\Users\\gustavo\\AppData\\Local\\Microsoft\\WindowsApps;C:\\Users\\gustavo\\AppData\\Local\\Programs\\Fiddler;C:\\Users\\gustavo\\AppData\\Local\\Microsoft\\WindowsApps;C:\\Users\\gustavo\\AppData\\Local\\Yarn\\bin;C:\\Users\\gustavo\\AppData\\Roaming\\npm;C:\\Users\\gustavo\\AppData\\Local\\Programs\\Microsoft VS Code Insiders\\bin'

In [142]: os.getenv('USERNAME')
Out[142]: 'gustavo'
````

```` python
In [144]: import sys

In [145]: sys.argv
Out[145]: ['C:\\Python39\\Scripts\\ipython']

In [147]: sys.platform
Out[147]: 'win32'

In [148]: sys.version
Out[148]: '3.9.0 (tags/v3.9.0:9cf6752, Oct  5 2020, 15:34:40) [MSC v.1927 64 bit (AMD64)]'

In [149]:
````

Regular expression

```` python
In [150]: import re

In [151]: if re.search('tang', 'tangerines'): print("tang is in tangerines")
tang is in tangerines

In [153]: if re.search('.ang', 'dangerines'): print("Matched!")
Matched!

In [154]: if re.search('.ang\w', 'dangerines'): print("Matched!")
Matched!

In [155]: angs = re.search('(.ang)', 'dangerines')

In [156]: angs.groups()
Out[156]: ('dang',)

In [157]: vowels_re = '[aeiou]'

In [158]: re.findall(vowels_re, 'dangerines')
Out[158]: ['a', 'e', 'i', 'e']

````

turtle

```` python
In [159]: import turtle

In [160]: turtle.fd(100)

In [161]: turtle.lt(90)

In [162]: turtle.fd(100)

In [163]: turtle.lt(90)

In [164]: turtle.fd(100)

In [165]: turtle.lt(90)

In [166]: turtle.fd(100)

In [167]: turtle.clear()

In [168]: def do_square(size):
     ...:     for i in range(4):
     ...:         turtle.fd(size)
     ...:         turtle.lt(90)
     ...:

In [169]: do_square(100)

In [170]: do_square(200)

In [171]: def do_triangle(size):
     ...:     for i in range(3):
     ...:         turtle.fd(size)
     ...:         turtle.lt(120)
     ...:

In [172]: do_triangle(75)

In [173]: turtle.color("orange")

In [174]: do_triangle(88)

In [175]: def do_poly(sides, size):
     ...:     for i in range(sides):
     ...:         turtle.fd(size)
     ...:         turtle.lt(360 / sides)
     ...:
     ...:

In [176]: do_poly(5, 75)

In [177]: do_poly(6, 120)

In [178]: do_poly(7, 120)

In [179]: do_poly(8, 120)

In [180]: do_poly(8, 120)
````

Python Packages from 3rd parties

https://pypi.org/

(packages contain modules, pip3 installs packages, import imports modules)

```` bash
pip3 install requests   
````

```` python
In [2]: import requests

In [3]: requests.get('http://nasa.gov')
Out[3]: <Response [200]>

In [6]: resp = requests.get('http://gud.ninja')

In [7]: resp.status_code
Out[7]: 200

In [8]: resp.text
Out[8]: '<html>\n\t<title>www GuDs website!</title>\n\t<body>\n\t\t<div align="center">\n\t\t\t<h1>Just a "Hi there" website!</h1>\n\t\t</div>\n\t</body>\n</html>'

In [9]: resp = requests.get('http://nasa.gov')

In [11]: len(resp.text)
Out[11]: 13411

In [6]: import requests

In [7]: meteor_resp = requests.get('https://data.nasa.gov/resource/gh4g-9sfh.json')

In [10]: meteor_resp.status_code
Out[10]: 200

In [15]: meteor_resp.json() 
...
{'name': 'Tomakovka',
  'id': '24019',
  'nametype': 'Valid',
  'recclass': 'LL6',
  'mass': '600',
  'fall': 'Fell',
  'year': '1905-01-01T00:00:00.000',
  'reclat': '47.850000',
  'reclong': '34.766670',
  'geolocation': {'latitude': '47.85', 'longitude': '34.76667'}}]


# https://www.findlatitudeandlongitude.com/  

````

distance on earth from long and lat

```` python
# haversine formula
import math

def calc_dist(lat1, lon1, lat2, lon2):
    lat1 = math.radians(lat1)
    lon1 = math.radians(lon1)
    lat2 = math.radians(lat2)
    lon2 = math.radians(lon2)

    h = math.sin( (lat2 - lat1) / 2 ) ** 2 + \
      math.cos(lat1) * \
      math.cos(lat2) * \
      math.sin( (lon2 - lon1) / 2 ) ** 2

    return 6372.8 * 2 * math.asin(math.sqrt(h))
````

```` python
In [23]: meteor_data[0]
Out[23]:
{'name': 'Aachen',
 'id': '1',
 'nametype': 'Valid',
 'recclass': 'L5',
 'mass': '21',
 'fall': 'Fell',
 'year': '1880-01-01T00:00:00.000',
 'reclat': '50.775000',
 'reclong': '6.083330',
 'geolocation': {'latitude': '50.775', 'longitude': '6.08333'}}

In [24]: # dist sao paulo SP, from Aachen Germany

In [25]: calc_dist(50.775000, 6.083330, -23.570222, -46.649344)
Out[25]: 9747.707007606487

In [26]: my_loc = (-23.570222, -46.649344)

In [29]: for meteor in meteor_data:
    ...:     if not ('reclat' in meteor and 'reclong' in meteor): continue
    ...:     meteor['distance'] = calc_dist(float(meteor['reclat']), float(meteor['reclong']), my_loc[0
    ...: ], my_loc[1])
    ...:

In [30]: meteor_data[0]
Out[30]:
{'name': 'Aachen',
 'id': '1',
 'nametype': 'Valid',
 'recclass': 'L5',
 'mass': '21',
 'fall': 'Fell',
 'year': '1880-01-01T00:00:00.000',
 'reclat': '50.775000',
 'reclong': '6.083330',
 'geolocation': {'latitude': '50.775', 'longitude': '6.08333'},
 'distance': 9747.707007606487}
````

Sort a dict by distance, when dont have distance, place infinity (put in the end of the list)

```` python
In [32]: def get_dist(meteor):
    ...:     return meteor.get('distance', math.inf)
    ...:

In [33]: meteor_data.sort(key=get_dist)

In [34]: meteor_data[0:10]
Out[34]:
[{'name': 'Angra dos Reis (stone)',
  'id': '2302',
  'nametype': 'Valid',
  'recclass': 'Angrite',
  'mass': '1500',
  'fall': 'Fell',
  'year': '1869-01-01T00:00:00.000',
  'reclat': '-22.966670',
  'reclong': '-44.316670',
  'geolocation': {'latitude': '-22.96667', 'longitude': '-44.31667'},
  'distance': 247.6208699598985},
 {'name': 'Marilia',
  'id': '15422',
  'nametype': 'Valid',
  'recclass': 'H4',
  'mass': '2500',
  'fall': 'Fell',
  'year': '1971-01-01T00:00:00.000',
  'reclat': '-22.250000',
  'reclong': '-49.933330',
  'geolocation': {'latitude': '-22.25', 'longitude': '-49.93333'},
  'distance': 367.0842200095451},

# last ones
In [35]: meteor_data[-1:-3:-1]
Out[35]:
[{'name': 'Talampaya',
  'id': '23791',
  'nametype': 'Valid',
  'recclass': 'Eucrite-cm',
  'mass': '1421',
  'fall': 'Fell',
  'year': '1995-01-01T00:00:00.000'},
 {'name': 'Dominion Range 03240',
  'id': '32592',
  'nametype': 'Valid',
  'recclass': 'LL5',
  'mass': '290.89999999999998',
  'fall': 'Found',
  'year': '2002-01-01T00:00:00.000'}]


# how many dont have distance
In [37]: len(meteor_data)
Out[37]: 1000

In [39]: len([m for m in meteor_data if 'distance' not in m ])
Out[39]: 12


````

Package Management

```` bash
pip3 install pipenv

# init package env, creates Pipfile
pipenv --three

Creating a virtualenv for this project…
Pipfile: C:\Gustavo\ToolBox\biblioteca\python\find_meteorities\Pipfile
Using C:/Python39/python.exe (3.9.0) to create virtualenv…
[=   ] Creating virtual environment...created virtual environment CPython3.9.0.final.0-64 in 6169ms
  creator CPython3Windows(dest=C:\Users\gustavo\.virtualenvs\find_meteorities-TjczjUYU, clear=False, global=False)
  seeder FromAppData(download=False, pip=bundle, setuptools=bundle, wheel=bundle, via=copy, app_data_dir=C:\Users\gustavo\AppData\Local\pypa\virtualenv)
    added seed packages: pip==20.2.3, setuptools==50.3.1, wheel==0.35.1
  activators BashActivator,BatchActivator,FishActivator,PowerShellActivator,PythonActivator,XonshActivator

Successfully created virtual environment!
Virtualenv location: C:\Users\gustavo\.virtualenvs\find_meteorities-TjczjUYU
Warning: Your Pipfile requires python_version 3.6, but you are using 3.9.0 (C:\Users\g\.\f\S\python.exe).
  $ pipenv --rm and rebuilding the virtual environment may resolve the issue.
  $ pipenv check will surely fail.

# enter virtual env
pipenv shell

# delete virtual env
pipenv --rm

# run a shell inside virtual env
pipenv run python -V 

pipenv run python meteors/find_meteors.py
     Traceback (most recent call last):
  File "C:\Gustavo\ToolBox\biblioteca\python\find_meteorities\meteors\find_meteors.py", line 2, in <module>
    import requests
ModuleNotFoundError: No module named 'requests'

# install package inside virt env
pipenv run pip3 install requests

pipenv run python meteors/find_meteors.py
Meteor Angra dos Reis (stone) Fell 248 km away on 1869
Meteor Marilia Fell 368 km away on 1971
Meteor Avanhandava Fell 413 km away on 1952
Meteor São Jose do Rio Preto Fell 417 km away on 1962
Meteor Conquista Fell 425 km away on 1965
Meteor Rio Negro Fell 425 km away on 1934
Meteor Ibitira Fell 433 km away on 1957
Meteor Mafra Fell 440 km away on 1941
Meteor Patrimonio Fell 491 km away on 1950
Meteor Sete Lagoas Fell 522 km away on 1908

# install package inside virt env as dev dependency
pipenv install -d ipython

pipenv run ipython

````


[packages]

requests = "*" <- latest info


Import modules

`import <file> from <folder>`

```` python
from meteors import find_meteors

#add to code, it will not run when importing the file but will run when files run as script
if __name__ == '__main__':


````

Boto3 -- aws cli

`pipenv install boto3`

```` python
import boto3

session = boto3.Session(profile_name='shotty')

#ec2 resource from boto3
ec2 = session.resource('ec2')

# list instances
for i in ec2.instances.all():
   print(i)

ec2.Instance(id='i-0be10bf011995dbbb')
ec2.Instance(id='i-0350f8452977b279e')
ec2.Instance(id='i-0f62d2b389e3ab676')

In [3]: inst = ec2.instances.all()

In [4]: inst
Out[4]: ec2.instancesCollection(ec2.ServiceResource(), ec2.Instance)

In [5]: list(inst)[0]
Out[5]: ec2.Instance(id='i-0be10bf011995dbbb')

In [6]: i = list(inst)[0]

In [7]: i.id
Out[7]: 'i-0be10bf011995dbbb'

In [8]: i.placement
Out[8]: {'AvailabilityZone': 'us-east-1a', 'GroupName': '', 'Tenancy': 'default'}

In [9]: i.state
Out[9]: {'Code': 16, 'Name': 'running'}
````

Converting return from instances

```` python
import boto3

session = boto3.Session(profile_name='shotty')

#ec2 resource from boto3
ec2 = session.resource('ec2')

# list instances
for i in ec2.instances.all():
   print(i)

inst = ec2.instances.all()

i = list(inst)[0]

i.tags
Out[5]: [{'Key': 'project', 'Value': 'Valkyrie2'}]

In [3]: inst = ec2.instances.all()

In [4]: i = list(inst)[0]

In [5]: i.tags
Out[5]: [{'Key': 'project', 'Value': 'Valkyrie2'}]

In [6]: tags = { t['Key']: t['Value'] for t in i.tags or [] }

In [7]: tags
Out[7]: {'project': 'Valkyrie2'}

In [4]: i = list(inst)[1]

In [5]: i.tags

In [6]: tags = { t['Key']: t['Value'] for t in i.tags or [] }

In [7]: tags
Out[7]: {}

In [4]: vols = ec2.volumes.all()

In [5]: for v in vols:
   ...:     print(v)
   ...:
ec2.Volume(id='vol-050b6ce4fe4b02350')
ec2.Volume(id='vol-045885c058086a2e5')
ec2.Volume(id='vol-06453dd5fc9039231')

from sh
````


Use a program in development inside ipython
```` python
In [6]: from shotty import shotty

In [7]: project = 'Valkyrie'

In [8]: instances = shotty.filter_instances(project)

In [10]: for i in instances:
    ...:     print(i)
    ...:
ec2.Instance(id='i-0e2c698caa86b840d')
ec2.Instance(id='i-0bd130da2f70e54ca')
ec2.Instance(id='i-01a3151c27b550ef9')

In [13]: for i in instances:
    ...:     print(i)
    ...:     for v in i.volumes.all():
    ...:         print(v)
    ...:
ec2.Instance(id='i-0e2c698caa86b840d')
ec2.Volume(id='vol-06453dd5fc9039231')
ec2.Instance(id='i-0bd130da2f70e54ca')
ec2.Volume(id='vol-045885c058086a2e5')
ec2.Instance(id='i-01a3151c27b550ef9')
ec2.Volume(id='vol-050b6ce4fe4b02350')
````
History shows all commands w/o line markers, good for coping into the bigger script
```` python
%history

for i in instances:
    print(i)
    for v in i.volumes.all():
        print(v)

````

Snapshots
```` python
In [20]: for i in instances:
    ...:     for v in i.volumes.all():
    ...:         for s in v.snapshots.all():
    ...:             snappy = s
    ...:

In [21]:

In [21]: snappy
Out[21]: ec2.Snapshot(id='snap-0e067ca26646c5b2e')

````

packaging and distributing

```` bash
# setting up
pipenv install -d setuptools

pip3 install setuptools

#package
pipenv run "python setup.py bdist_wheel"

#win
pipenv run python setup.py bdist_wheel
````

install
```` bash
pip3 install dist/snapshotalyzer_30000-0.1-py3-none-any.whl

#check install
pip3 show snapshotalyzer_30000
````

uninstall

```` bash
pip3 uninstall snapshotalyzer_30000
````

install from custom
```` bash
pip3 install http://www.gud.ninja/snapshotalyzer_30000-0.1-py3-none-any.whl
````

```` python
````

```` python
````

```` python
````

```` python
````

```` python
````

```` python
````

```` python
````

```` python
````

```` python
````

```` python
````

```` python
````

```` python
````

```` python
````

```` python
````

```` python
````

```` python
````

```` python
````




