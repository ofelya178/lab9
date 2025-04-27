import math

def phi(x):
    return math.atan(x**(1/3))

x0 = 0.5  # İlkin təxmin
epsilon = 1e-5  # Dəqiqlik
max_iter = 1000  # Maksimum iterasiya sayı

for i in range(max_iter):
    x1 = phi(x0)
    if abs(x1 - x0) < epsilon:
        break
    x0 = x1

print("Təqribi kök:", x1)
