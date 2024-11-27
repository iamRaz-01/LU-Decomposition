# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
(i) To find the L and U matrix
1. **Import Libraries**: Import `numpy` for handling arrays and `lu` from `scipy.linalg` for LU decomposition.
   ```python
   import numpy as np
   from scipy.linalg import lu
   ```

2. **Input the Matrix**: Convert user input into a `numpy` array using `eval(input())`.
   ```python
   A = np.array(eval(input()))
   ```

3. **Perform LU Decomposition**:
   - Use `lu(A)` to decompose matrix `A` into:
     - \( P \): Permutation matrix (optional, not used here).
     - \( L \): Lower triangular matrix.
     - \( U \): Upper triangular matrix.
   ```python
   P, L, U = lu(A)
   ```

4. **Print Results**: Display the \( L \) and \( U \) matrices.
   ```python
   print(L)
   print(U)
   ```
(ii) To find the LU Decomposition of a matrix
1. **Import Libraries**: Import `numpy` for array handling and `lu_factor`/`lu_solve` from `scipy.linalg` for LU decomposition and solving.
   ```python
   import numpy as np
   from scipy.linalg import lu_factor, lu_solve
   ```

2. **Input the Coefficient Matrix and Constants**:
   - Use `eval(input())` to take user input for the coefficient matrix `a` and the constants vector `b`.
   ```python
   a = np.array(eval(input()))  # Coefficient matrix
   b = np.array(eval(input()))  # Constants vector
   ```

3. **LU Factorization**:
   - `lu_factor(a)` computes the LU decomposition of matrix `a` and returns:
     - \( LU \): Combined representation of the \( L \) (lower triangular) and \( U \) (upper triangular) matrices.
     - `piv`: Pivot indices for row permutations.
   ```python
   lu, piv = lu_factor(a)
   ```

4. **Solve the System**:
   - `lu_solve((lu, piv), b)` uses the LU decomposition to solve \( Ax = b \) for \( x \).
   ```python
   x = lu_solve((lu, piv), b)
   ```

5. **Print the Solution**:
   - Display the solution \( x \), which is the values of the variables that satisfy the equations.
   ```python
   print(x)
   ```
## Program:
(i) To find the L and U matrix
```python
'''Program to find L and U matrix using LU decomposition.
Developed by: Abdul Rasak N 
RegisterNumber: 24002896
'''
import numpy as np 
from scipy.linalg import lu 
A = np.array(eval(input()))
P,L,U = lu(A)
print(L)
print(U)


```
(ii) To find the LU Decomposition of a matrix
```python
'''Program to solve a matrix using LU decomposition.
Developed by: Abdul Rasak N
RegisterNumber: 24002896
'''

# To print X matrix (solution to the equations)
import numpy as np
from scipy.linalg import lu_factor, lu_solve
a = np.array(eval(input()))
b = np.array(eval(input()))
lu , piv = lu_factor(a)
x = lu_solve((lu,piv),b)
print(x)
```

## Output:
(i) To find the L and U matrix
![image](https://github.com/user-attachments/assets/b22be0db-4252-4437-b7b3-dc859ecfc120)

(ii) To find the LU Decomposition of a matrix
![image](https://github.com/user-attachments/assets/684460d6-1859-4d6b-8497-1dd073f12e6b)



## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.

