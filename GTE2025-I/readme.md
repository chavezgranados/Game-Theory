# Bienvenidos al curso!

*Curso dirigido a la USMP (PE)*

**Solución numérica:**

# Mi código Python para encontrar la raíz

```python
from scipy.optimize import root
import numpy as np

def equation_to_solve(a):
  return 100/(1+a) - (2*a)*np.exp(a**2+3)

initial_guess = 1.0
solution = root(equation_to_solve, initial_guess)

if solution.success:
  print(f"The value of a is approximately: {solution.x[0]}")
else:
  print("Could not find a solution with the given initial guess.")

solution.message

