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

a=5
if a%2==0:
   print('a is even')
elif a%2==1:
   print('a is odd')

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

a = [1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]
b = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13]
c=list(set(a).intersection(set(b)))
print(c)
d=list(set(a).difference(set(b)))
print(d)


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


#Assignment 3

import numpy as np
import matplotlib.pyplot as plt
x = np.linspace(0, 10, 50)
y = 4 + 2*x - x**2 + 0.075*x**3
plt.plot(x,y)
plt.show()

noise = np.random.normal(0,1.5,50)
y_with_noise = 4 + 2*x - x**2 + 0.075*x**3 + noise
plt.plot(x,y_with_noise)
plt.show()

x = np.linspace(0, 10, 50)
y = 4 + 2*x - x**2 + 0.075*x**3
y_with_noise = 4 + 2*x - x**2 + 0.075*x**3 + noise
plt.scatter(x,y_with_noise)
plt.plot(x,y)
plt.show()

plt.scatter(x,y_with_noise,color='black')
plt.plot(x,y,color='blue')
plt.xlabel('x',fontsize=16)
plt.ylabel('y',fontsize=16)
plt.title('matplotlib-plot',fontsize=16)
plt.show()
plt.savefig('matplotlib-plot.png')

x = np.linspace(0, 10, 50)
y = 4 + 2*x - x**2 + 0.075*x**3
y_with_noise = 4 + 2*x - x**2 + 0.075*x**3 + noise
fig = plt.figure()
ax = fig.add_subplot(1, 1, 1)
ax.plot(x,y,color='blue')
ax.scatter(x,y_with_noise,color='black')
ax.set_xlabel('x', fontsize=16)
ax.set_ylabel('y', fontsize=16)
ax.set_title('figure-plot', fontsize=16)
ax.set_save('figure-plot.png')
plt.show()

import pandas as pd
a = pd.read_csv('anscombe.csv')
a
a.head(2)
a.tail(2)
a.info()
a.columns
a.dtypes
a.describe()
a['dataset']
a.iloc[0:10]

b=a.loc[a['dataset'] == 'III']
b
b.plot(x='x',y='y',kind='line')
b.plot(x='x',y='y',kind='scatter')
c=a.loc[a['dataset'] == 'I']
c.plot(x='x',y='y',kind='scatter')
d=a.loc[a['dataset'] == 'II']
d.plot(x='x',y='y',kind='scatter')
e=a.loc[a['dataset'] == 'IV']
e.plot(x='x',y='y',kind='scatter')

from sklearn.linear_model import LinearRegression
X=a['x'].values.reshape(-1,1)
Y=a['y'].values.reshape(-1,1)
reg=LinearRegression()
reg.fit(X,Y)
plt.scatter(X,Y,color='black')
plt.plot(X,reg.predict(X),color='blue')
plt.xlabel('x',fontsize=16)
plt.ylabel('y',fontsize=16)
plt.title('anscombe-I',fontsize=16)
plt.show()
plt.savefig('anscombe-I.png')
