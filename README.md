# F202
Room for students

import sympy as smp
import numpy as np
import matplotlib.pyplot as plt
x_val = np.genfromtxt('hw1.txt')
x = smp.symbols('x')
func = x**2 + 2*x + 1
f_val = np.zeros(100)
i = 0
for val in x_val:
    f_val[i] = func.subs([(x,val)]) 
    i = i + 1
def f(x):
    return x**2 + 2*x + 1
fig = plt.figure()
plt.plot(x_val, f_val, label='linear line', color = 'red', linewidth=2)
plt.xlabel('x axis')
plt.ylabel('y axis')
plt.legend()
plt.title("AkerkeB's first plot")
plt.show()
fig.savefig("akerkeb'sfig.pdf")
