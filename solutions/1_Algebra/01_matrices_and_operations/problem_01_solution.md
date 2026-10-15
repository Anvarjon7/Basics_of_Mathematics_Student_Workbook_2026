# Exercise 1: Matrix Size and Entries

## Question

Given the matrices

$$
A=\begin{pmatrix}
2 & -1 & 3\\
0 & 4 & 5
\end{pmatrix},
\qquad
B=\begin{pmatrix}
1 & 0\\
-2 & 3\\
4 & 1
\end{pmatrix}.
$$

1. State the sizes of matrices \(A\) and \(B\).
2. Read off the entries \(a_{12}\), \(a_{23}\), \(b_{21}\), and \(b_{32}\).
3. Write the second row of \(A\) and the first column of \(B\) as vectors.

## Solution

### 1. Sizes of Matrices \(A\) and \(B\)

**Method:** The size of a matrix is written as \(m\times n\), where \(m\) is the number of rows and \(n\) is the number of columns.

**Matrix \(A\):**

Matrix \(A\) has 2 rows and 3 columns. Therefore, its size is

$$
\boxed{A\text{ is }2\times3}
$$

**Matrix \(B\):**

Matrix \(B\) has 3 rows and 2 columns. Therefore, its size is

$$
\boxed{B\text{ is }3\times2}
$$

**Verification:** An \(m\times n\) matrix contains \(m\cdot n\) entries.

- Matrix \(A\): \(2\cdot3=6\) entries.
- Matrix \(B\): \(3\cdot2=6\) entries.

Both counts match the given matrices.

### 2. Reading Matrix Entries

**Method:** The entry \(m_{ij}\) refers to the element in row \(i\) and column \(j\). The row index comes first, followed by the column index.

Reading the entries directly from the matrices:

- \(a_{12}=-1\): row 1, column 2 of \(A\).
- \(a_{23}=5\): row 2, column 3 of \(A\).
- \(b_{21}=-2\): row 2, column 1 of \(B\).
- \(b_{32}=1\): row 3, column 2 of \(B\).

Therefore,

$$
\boxed{
a_{12}=-1,\quad
a_{23}=5,\quad
b_{21}=-2,\quad
b_{32}=1
}
$$

**Verification:** Each entry was identified using its row and column indices in the corresponding matrix.

### 3. Row and Column Vectors

**Method:** A row vector lists entries horizontally, while a column vector lists entries vertically.

**Second row of \(A\):**

The second row of \(A\) contains the entries \(0\), \(4\), and \(5\). Written as a row vector,

$$
\boxed{
r_2(A)=\begin{pmatrix}0&4&5\end{pmatrix}
}
$$

Its size is \(1\times3\), matching the three columns of \(A\).

**First column of \(B\):**

The first column of \(B