# IT-exam
import random
import sys
from itertools import *
# sys.setrecursionlimit(10000)
def binary_search(list1, item):
    low = 0
    high = len(list1) - 1
    while low <= high:
        mid = (low + high) // 2
        num = list1[mid]
        if num < item:
            low = mid + 1
        elif num > item:
            high = mid - 1
        else:
            return mid
    return None

def tr(num):
    s = ''
    while num > 0:
        s = str(num % 8) + s
        num //= 8
    return s






def f(num):
    chet = 0
    nechet = 0
    mas = []
    for i in range(150):
        i = tr(i)
        for n in i:
            if int(n) % 2 == 0:
                chet += 1
            else:
                nechet += 1
        if chet > nechet:
            i += '22'
        else:
            i += '11'
        mas.append(i)
"""""
mass = []
for N in range(10,1000):
    R = tr(N)
    chet = 0
    nech = 0
    for symb in R:
        if symb % 2 == 0:
            chet += 1
        else:
            nech += 1
    if chet > nech:
        R = '22' + R
    else:
        R = '11' + R
"""""


mass = []
for i in range(10):
    a = random.randint(1,10)
    mass.append(a)

print(mass)    
a = mass[0]
for i in range(len(mass) - 1):
    mass[i] = mass[i+1]
mass.remove(mass[-1])
mass.append(a)
print(mass)
















