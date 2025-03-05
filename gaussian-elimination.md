make the multiple linear equation
form as `reduced row form` the `row echelon form` is a matrix form that follows
some rules. 
1. Each row first `non-zero` element called as `pivot` or `leading
entry` consist with appears to the right of the pivot in the row above.
2. All entry or elements below pivot consist with zero.
3. If there is full of zero row it consist with at the bottom

`row echelon form`
$$
\begin{bmatrix}
1 & 5 & 7\\
0 & 1 & 2\\
0 & 9 & 1
\end{bmatrix}
$$


$
\begin{cases}
x+2y+4z=7\\
3x+7y+2z=-11\\
2x+3y+3z=1
\end{cases}
$

Gaussian Elimination uses row operations
1. swapping rows, swap two rows 2. multiple a row
3. add or subract one row from another

converted the equations into an `augmented matrix`, extracting coefficient
constant

$\begin{matrix} 1 & 2 & 4 & | & 7\\ 3 & 7 & 2 & | & -11\\
2 & 3 & 3 & | & 1\\
\end{matrix}
$

by using row operations make all elements under each pivot(leading entry) to zero.

The first row's pivot is 1, converts the below 3 and 2 to zero.
Subtract with Row 1 multipled by 3 to make 3 to 0(3 - 3(1) = 0)
    
denote as

$R_2\to R_2 - 3R_1$

results:

$\begin{matrix}
1 & 2 & 4 & | & 7\\
0 & 1 & -10 & | & -32\\
2 & 3 & 3 & | & 1\\
\end{matrix}$

then eliminate the third row fist columnk, 2 to 0 with subtracting the first row
by multipled 2(2 - 2(1) = 0)

$\begin{matrix}
1 & 2 & 4 & | & 7\\
0 & 1 & -10 & | & -32\\
0 & -1 & -5 & | & -13\\
\end{matrix}$

In the second row, the pivot is 1, which is directly next to the first row's
pivot (1). It follows the second rule of `row echelon form`.

same as previous under the second row's leading entry consist with consist with
zero, so using row operations again converted the `-1` to zero.

$R_3 \to R_3 + R_2$

$\begin{matrix}
1 & 2 & 4 & | & 7\\
0 & 1 & -10 & | & -32\\
0 & 0 & -15 & | & -45\\
\end{matrix}$

finally the matrix forms with `row echelon fomr`,

now we apply `Back Substitution`

if we converted the row 3 to equation

$0x + 0y -15z = -45$
which we could get the value of `z`


$z=\frac{-45}{-15}= 3$

now we have value of `z`, substitute it into backward row.


$0x + 1y + -10(3) = -32$

$y = -32 + 30 = -2$
backward row, now find value of `x`

$1x + 2(-2) + 4(3) = 7$

$x = 7 - 8 = -1$

according to the python, all equations holds true
when we substitute the variables, result correctly.
This confirms the solution is correct,
Gaussian Elimination is indeed correct.
