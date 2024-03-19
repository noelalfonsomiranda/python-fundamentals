# python-fundamentals
[![My Skills](https://skillicons.dev/icons?i=py)](https://skillicons.dev)
---
source: [Corey Schafer](https://www.youtube.com/@coreyms)

### Helpers
```python
print(help(str))
print(type(var))
print(dir(var)) #available methods modules
print(var `comparison` var)
print(id(var))

import sys
print(sys.path)

pass #placeholder for future, does nothing, like return in JS

import builtins #standard modules of python
print(dir(builtins))
```

### String
```python
greeting = 'Hello'
name = 'Foo'
message = f'{greeting}, {name.upper()}, Welcome!'
message = message.replace('Hi', Hello)
print(message)
print(len(message)) #length of string
print(message[0]) #print single string
print(message[0:5]) #range of string
print(message[6:]) #starting until the end
print(message[5:%])
print(message.count('c'))  #count character in a string
print(message.find('World')) #print start string index
```

### Integers and Floats
```python
.2f #2 decimal
print(3 * (1 + 2)) #9

num = 1
num += 1 #2
num *= 10 #10
print(abs(-3)) #3
print(round(3.75)) #4
print(round(3.75, 1)) #3.8

num_1 = '100'
num_2 = '200'
num_1 = int(num_1)
num_2 = int(num_2)
print(num_1 + num_2)
```

### Lists (mutable)
``` python
empty_list = list()
list = [array]
print(list[3])
print(list[-1]) #last item
print(list[0:2]) #after the beginning and last item
print(list[6:]) #starting until the end

list.append('test') #add to last
list.insert(0, 'test') #insert by index
list.extend(list2) #merge arrays
list.append(list2) #insert array into array
list.remove('item')
list.pop() #remove and return last value of list
list.reverse()
list.sort() #asc order
list.sort(reverse=True) #desc order
sorted_list = sorted(list) #prevent altering
print(min(list)) #get min num
print(max(list)) #get max num
print(sum(list)) #add list
print(list.index('item')) #get index of an item
print('item' in list) #returns bool

list = [5,2,3,1,4]
s_list = sorted(list) #prevent altering
s_list = sorted(list, reverse=True) #desc order
list.sort() #sort original value

for item in list:
  print(item)

for index, item in enumerate(list):
  print(index, item)

for index,item in enumerate(list,start=1):#start index to 1
  print(index, item)

list_str = ', '.join(list) #return as string
new_list = list_str.split(', ') #return as array

list = [-5,2,3,1,-4, -6]
s_list = sorted(list, key=abs)
```

### Tuples (immutable) 
``` python
#instead of [] use ()
empty_tuples = tuple()

tuple = (5,2,3,1,4)
s_tuple = sorted(tuple)
```

### Sets
``` python
#insted of [] use {}, random sorting, remove duplicates

empty_sets = set()
print(list1.intersection(list2)) #get both present items
print(list1.difference(list2)) #return not the same
print(list1.union(list2)) #return all items remove duplicates
```

### Dictionaries
``` python
dictionaries = {'name', 'John', 'age': 30, programming: ['Python', 'JavaScript']}
print(dictionaries['name'])
print(dictionaries.get('phone', 'Not Found'))

dictionaries['phone'] = 5555-5555 #add key value pair
dictionaries['name'] = 'Foo' #update value of key
dictionaries.update({'name', 'Bar', 'age': 20, 'phone': '4444-4444'}) #update/add dictionaries
del dictionaries['phone'] #delete prop
age = dictionaries.pop('age') #remove from dictionary and return new value from var
print(len(dictionaries)) #return count keys
print(dictionaries.keys())
print(dictionaries.values())
print(dictionaries.items())

dictionary = {'name': 'John', 'job': 'SE', 'age': None}
s_dictionary = sorted(dictionary) #sort the keys

for key in dictionaries:
  print(key)

for key, value in dictionaries.items():
  print(key, value)
```

### Conditional and Booleans, If Else ElIf statements
``` python
#python don't have switch statement
#operators - and, or, not, is
#is - comparison object in memory
if not True:
  print(False)
elif condition == 'pass' and True:
  print(True)
elif condition == 'pass':
  print(True)
else:
  print(False)

a = [1,2,3]
b=a #to have actually the same value with same id
print(id(a))
print(id(b))
print(a is b) #comparison like ==

# False values
# False
# None
# Zero of any numeric type
# Any empty sequence. '', (), []
# Any empty mapping {}
condition = False
if condition:
  print(True)
else:
  print(False) #will fall into else
```

### Loops and Iterations - For/While Loops
``` python
nums = [1,2,3,4]
for num in nums:
  if num == 3:
    print('Found it!')
    break #print start until break part and replace value
    continue #print start, replace value and continue
  print(num)

# loop within a loop
for num in nums:
  for letter in 'abc':
    print(num, letter)

for i in range(10):
  print(i) #return 0 to 9
range(1, 11) #return 1 to 10

x = 0
while x < 10
  if x == 5:
    break #prevents infinite loop
  print(x)
  x += 1 #when reach the value of x to 9, stop, when reach 10 break
```

### Functions
``` python
def hello_func(greeting, name='You'): #will get an error when nothing passed parameter
  pass #keyword prevent error, empty func, dumb func, returns None
  print('hello func')
  return '{}, {}.'.format(greeting, name)

print(hello_func)
print(hello_func())
print(hello_func('hi', name='John').upper())
hello_func()

def student_info(*args, **kwargs):
  print(args)
  print(kwargs)

student_info('Math', 'Art', name='Foo', age=22)
courses = ['Math', 'Art]
student = {name='Foo', age=22}
student_info(*courses, **student)
```

### Import Modules and Exploring The Standard Library
``` python
import my_module
import my_module as any_name
from my_module import find_index as fi, var_name
from my_module import * #can't trackdown imported modules, var

courses = ['History', 'Math', 'Physics', 'IT']
index = my_module.find_index(courses, 'Math')
index = mm.find_index(courses, 'Math')
print(index) #return 1

import sys
sys.path.append('/MyPath')

#will add to sys.path
mac:
.bash_profile
export PYTHONPATH="/MyPath" #will add to sys.path
win:
System Properties > Environment Variables > New User Variable

import random
random_course = random.choice(courses)
print(random_course) #return random value

import math
rads = math.radians(90)
print(math.sin(rads)) #return 1.0 is the sin of 90 degrees

import datetime
import calendar
today = datetime.date.today()
print(today)
print(calendar.isLeap(2020)) #return True, bool
```

### OS Module - Use Underlying Operating System Functionality
``` python
import os
print(os.getcwd()) #scan system, add files, delete files
print(os.__file__) #path to view python libraries, like antigravity, webbrowser
import antigravity #comic for python
```

### File Objects - Reading and Writing to Files
``` python
with open('test.txt', 'r') as f:
  pass #does nothing, for future
  for line in f: #efficient to return all file line contents
    print line(line, end='')
  f_contents = f.read() #f.readlines() - minified contents, #f.readline() - return line by line
  f_contents = f.read(100) #100 is to return the size
  f_contents = f.read(100) #continue to return the content
  f_contents = f.read(100) #return empty string since reach the whole content
  print(f_contents) #return contents of file
  print(f_contents, end='') #remove empty next line
print(f.closed) #return bool

size_to_read = 100
f_contents = f.read( size_to_read)
print(f.tell()) #10th position of the file where you read last of the file
f.seek(0) #repeat where you want to begin again with
while len(f_contents) > 0:
  print(f_contents, end='')
  f_contents = f.read( size_to_read)

f = open('test.txt', 'r+') #w-write,r-read,a-append,r+-rwa
print(f.name) #mode - open file for reading
f.close()

with open('test2.txt', 'w'): #create/override file contents
  f.write('Test')
  f.write('Test') #TestTest
  f.seek(0)
  f.write('Test') #Rest

# copy file .txt
with open('test.txt', 'r') as rf: #read file
  with open('test_copy.txt', 'w') as wf: #write file
    for line in rf:
      wf.write(line)

# copy image #add b on file mode
with open('test.txt', 'rb') as rf: #read file
  with open('test_copy.txt', 'wb') as wf: #write file
    for line in rf:
      wf.write(line)

# copy image #loop
with open('test.txt', 'rb') as rf: #read file
  with open('test_copy.txt', 'wb') as wf: #write file
    chunk_size = 4096
    rf_chunk = rf.read(chunk_size)
    while len(rf_chunk) > 0:
      wf.write(rf_chunk)
      rf_chunk = rf.read(chunk_size) #prevent infinite loop

    for line in rf:
      wf.write(line)
```

### Datetime Module - How to work with Dates, Times, Timedeltas, and Timezones
``` python
import datetimed = datetime.date(2015, 3, 23) #03 will get errorprint(d) #return 2016-03-10today = datetime.date.today()
print(today.year) #year day month, weekday() - starts 0 to 6, isoweekday() - starts 1 to 7
time_delta = datetime.timedelta(days=7)print(today + time_delta) #+ add or - minus
bday = datetime.date(2016, 9, 24)till_bday = bday - todayprint(till_bday) #till_bday.days, till_bday.total_seconds()
t = datetime.time(9, 19, 30, 99999) #hours, minutes, seconds, milli secondsprint(t) #t.hourdt = datetime.date(2016, 3, 19, 9, 19, 30, 99999) #year, month, day, hours, minutes, seconds, milli secondsprint(t) #t.hourtime_delta = datetime.timedelta(hours=12)print(dt + time_delta)print(dt) #full date, datetime.date is better, dt.date(), dt.time() dt.year
date = datetime.datetime.today() #today(), now(), utcnow() - timezone, same valueimport pytz #timezone third party librarydt = datetime.datetime(2016, 3, 19, 9, 19, 30, tzinfo=pytz.UTC)
print(dt) #return datetime+UTC
date_now = datetime.datetime.now(tz=pytz.UTC) #return datetime+milli seconds+ UTC
print(dt.isoformat())print(dt.strftime('%B %d, %Y')) #Month day, year
print(datetime.datetime.strptime('July 26, 2016',  '%B %d, %Y')) #format, second args what the value format
```

### Variable Scope - Understanding the LEGB rule and global/nonlocal statements
``` python
#LEGB - Local within function, Enclosing - var local scope, Global - var top, Built-in - reassign var
x = 'global x' #top
def test(z):
  global x #set as global even not on top
  y = 'local y'
  x = 'local x'
  print(x)
  print(z)
test('local z')
print(x)

def outer(): #enclosing
  x = 'outer x'
  def inner():
    nonlocal x #get outer var
    x = 'innex x'
    print(x)
  inner()
  print(x)
outer() #return outer x and inner x
```

### Using Try/Except Blocks for Error Handling
``` python
try:
  pass
except Exception:
  pass
else:
  pass
finally:
  pass

try:
  f = open('test.txt')
  var = bad_var
  if f.name == 'corrupt.txt':
     raise Exception #trigger the except Exception #raise the Exception
except FileNotFoundError as err: #general exception
#except Exception:
  print(err, 'Not Found')
except Exception as err:
  print(err, 'Went wrong.')
else:
  print(f.read())
  f.close()
finally: #always execute
  print('Executing Finally...')
```
