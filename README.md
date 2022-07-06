# csx4501
I'm Zhou Jingyi, a Chinese Junior majoring in economics. Ilove data scinece but haven't take much courses before, so I want to take this opportunity to learn about basic thoughts of data science and some useful data processing tools.

x = 5
y = 10
print('x + y =', x+y) 
print('x - y =', x-y)
print('x * y =', x*y)
print('x / y =', x/y) 
print('x // y =', x//y) 
print('x % y =', x%y)

a = [1,1,2,3,5,8,13,21,34,55,89]
print(a)
print(a[0])
print(a[5])
print(a[11])
print(a)
print(len(a))
a.reverse()
print(a)

a = [1,1,2,3,5,8,13,21,34,55,89] 
n=8
b=[i for i in a if i<n]
print(b)
a.append(144)
print(a)

# Using the below lists
# 1. print out all the elements that are contained in both lists
# 2. print out the elements that are contained in either list a or list b but not both
a = [1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]
b = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13]
c=list(set(a).intersection(set(b)))
print(c)
d=list(set(a).difference(set(b)))
print(d)

# Using the below dictionary
# add a new item to the dictionary,
# print an element from the dictionary,
# print out the message "<key> has <value> letters" for every <key>/<value> pair

a = {'January': 7, 'February': 8, 'March': 5, 'April': 5}
a['May'] = 6
print(a)
print(a['January'])
print(<i> has <j> letters for )

print(a)
b=a[0]
print(b)
c=a[11]
print(c)
join(a,c)

s=input('sno939us')
a=len(s)
i=0
count=1
while i <=(a/2):
    if s[i]==s[a-i-1]:
        count=1
        i+=1
    else:
    count=0
    break
if count==1:
    print('Yes')
else:
    print('No')
    
 # Write a function that sets a random seed and prints three random numbers between 0 and 1
# You may find it useful to look up:
# random.seed and random.random
import random  
   import random
random.seed(1)
a = random.randint(0,1)
print(a)
b = random.uniform(0,1) 
print(b)
c= random.randrange(0,1,1)
print(c)

# Write a function that takes an integer as input
# and prints a random alphabetical character, alphabetical string,
# and alphabetical string of a fixed length equal to the input integer.
# You may find it useful to look up:
# string.ascii_letters, random.randint, random.choice
import random
import string
n=8
a=string.ascii_letters
print(a)
seed="abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ"
str1 = []
for i in range(n):
  str1.append(random.choice(seed))
StringS = ''.join(str1)
print(StringS)
