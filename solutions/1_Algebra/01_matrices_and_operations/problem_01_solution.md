# Exercise 1: Matrix Size and Entries

## 1. Problem Statement

Given the matrices:

$$
A = \begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5
\end{pmatrix},
\qquad
B = \begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1
\end{pmatrix}
$$

1. State the sizes (dimensions) of matrices $A$ and $B$.
2. Read off the specific entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

---

## 2. Theoretical Background and Concepts

### What is a Matrix?
A **matrix** is simply a rectangular table (or grid) of numbers arranged in horizontal **rows** and vertical **columns**, enclosed in parentheses or brackets:
* **Rows** run horizontally (from left to right $\leftrightarrow$). Think of rows of desks in a classroom or rows of seats in a cinema.
* **Columns** run vertically (from top to bottom $\updownarrow$). Think of tall pillars (columns) holding up a building.

### Matrix Size ($m \times n$)
The size or dimension of a matrix is always given as:
$$
\text{Size} = (\text{number of rows}) \times (\text{number of columns}) = m \times n
$$
> **Memory Trick:** Remember **RC** (like **R**adio **C**ontrol or **R**ow then **C**olumn). Rows are always counted first, columns second.

### Entry Addresses ($a_{ij}$)
Individual numbers inside a matrix are called its **entries** (or elements).
An entry is labeled $a_{ij}$, where:
* $i$ is the **row number** (counting down from top: $1, 2, \dots$),
* $j$ is the **column number** (counting across from left: $1, 2, \dots$).

For example, $a_{12}$ means: *"Go to Row 1, then move to Column 2"*.

### Row and Column Vectors
* A **row vector** is a matrix with only 1 row (size $1 \times n$), written horizontally: $\begin{pmatrix} x_1 & x_2 & \dots & x_n \end{pmatrix}$.
* A **column vector** is a matrix with only 1 column (size $m \times 1$), written vertically: $\begin{pmatrix} y_1 \\ y_2 \\ \dots \\ y_m \end{pmatrix}$.

---

## 3. Detailed Step-by-Step Solution

### Step 1: Determine the Sizes of $A$ and $B$

* **For Matrix $A$:**
  $$
  A = \begin{pmatrix}
  2 & -1 & 3 \\
  0 & 4 & 5
  \end{pmatrix}
  $$
  * Count the horizontal rows:
    * Row 1: $(2,\ -1,\ 3)$
    * Row 2: $(0,\ 4,\ 5)$
    $\implies 2$ rows ($m = 2$).
  * Count the vertical columns:
    * Column 1: $\begin{pmatrix} 2 \\ 0 \end{pmatrix}$, Column 2: $\begin{pmatrix} -1 \\ 4 \end{pmatrix}$, Column 3: $\begin{pmatrix} 3 \\ 5 \end{pmatrix}$
    $\implies 3$ columns ($n = 3$).

  $$
  \boxed{\text{Size of } A \text{ is } 2 \times 3}
  $$

* **For Matrix $B$:**
  $$
  B = \begin{pmatrix}
  1 & 0 \\
  -2 & 3 \\
  4 & 1
  \end{pmatrix}
  $$
  * Count the horizontal rows:
    * Row 1: $(1,\ 0)$
    * Row 2: $(-2,\ 3)$
    * Row 3: $(4,\ 1)$
    $\implies 3$ rows ($m = 3$).
  * Count the vertical columns:
    * Column 1: $\begin{pmatrix} 1 \\ -2 \\ 4 \end{pmatrix}$, Column 2: $\begin{pmatrix} 0 \\ 3 \\ 1 \end{pmatrix}$
    $\implies 2$ columns ($n = 2$).

  $$
  \boxed{\text{Size of } B \text{ is } 3 \times 2}
  $$

---

### Step 2: Read Off the Requested Entries

Using the rule "Row first, Column second" ($m_{ij} = \text{Row } i, \text{ Column } j$):

1. **Find $a_{12}$** in matrix $A$:
   * Go to Row 1: $(2,\ -1,\ 3)$.
   * Select Column 2: the entry is $-1$.
   $$a_{12} = -1$$

2. **Find $a_{23}$** in matrix $A$:
   * Go to Row 2: $(0,\ 4,\ 5)$.
   * Select Column 3: the entry is $5$.
   $$a_{23} = 5$$

3. **Find $b_{21}$** in matrix $B$:
   * Go to Row 2: $(-2,\ 3)$.
   * Select Column 1: the entry is $-2$.
   $$b_{21} = -2$$

4. **Find $b_{32}$** in matrix $B$:
   * Go to Row 3: $(4,\ 1)$.
   * Select Column 2: the entry is $1$.
   $$b_{32} = 1$$

$$
\boxed{a_{12} = -1, \quad a_{23} = 5, \quad b_{21} = -2, \quad b_{32} = 1}
$$

---

### Step 3: Write Row and Column Vectors

1. **Second row of $A$ as a vector:**
   * Extract the entire second horizontal line of $A$: the numbers are $0, 4, 5$.
   * A row vector is written horizontally:
   $$
   \boxed{r_2(A) = \begin{pmatrix} 0 & 4 & 5 \end{pmatrix}}
   $$
   * Its size is $1 \times 3$ (1 row, 3 columns).

2. **First column of $B$ as a vector:**
   * Extract the entire first vertical column of $B$: the numbers are $1, -2, 4$.
   * A column vector is written vertically:
   $$
   \boxed{c_1(B) = \begin{pmatrix} 1 \\ -2 \\ 4 \end{pmatrix}}
   $$
   * Its size is $3 \times 1$ (3 rows, 1 column).

---

## 4. Verification and Consistency Checks

* **Total entry count test:**
  * For any $m \times n$ matrix, total entries $= m \cdot n$.
  * Matrix $A$: $2 \times 3 = 6$ entries. Counting them individually: $2, -1, 3, 0, 4, 5$ (6 entries $\checkmark$).
  * Matrix $B$: $3 \times 2 = 6$ entries. Counting them individually: $1, 0, -2, 3, 4, 1$ (6 entries $\checkmark$).
* **Vector length checks:**
  * Second row $r_2(A)$ has length 3, matching the number of columns of $A$.
  * First column $c_1(B)$ has length 3, matching the number of rows of $B$.
* **Coordinate check:**
  * In $r_2(A)$, the elements are $a_{21}=0$, $a_{22}=4$, $a_{23}=5$. This matches Row 2 of $A$.
  * In $c_1(B)$, the elements are $b_{11}=1$, $b_{21}=-2$, $b_{31}=4$. This matches Column 1 of $B$.

---

## 5. Common Mistakes to Avoid

1. **Swapping rows and columns:** Writing $A$ as $3 \times 2$ instead of $2 \times 3$. Always remember: count how many rows (horizontal lines) first, then how many columns (vertical lines).
2. **Reversing entry indices:** Confusing $a_{12}$ with $a_{21}$. $a_{12}$ is Row 1 Column 2 ($-1$), whereas $a_{21}$ is Row 2 Column 1 ($0$).
3. **Writing column vectors horizontally:** A column vector must be written vertically $\begin{pmatrix} 1 \\ -2 \\ 4 \end{pmatrix}$, not horizontally, unless an explicit transpose symbol is used: $\begin{pmatrix} 1 & -2 & 4 \end{pmatrix}^T$.

---

## 6. How I Would Explain This in Class (Oral Summary)

> *"To find the size of any matrix, we count horizontal rows first and vertical columns second: Matrix $A$ has 2 rows and 3 columns, so it is $2 \times 3$, while $B$ has 3 rows and 2 columns, making it $3 \times 2$. To locate an entry like $a_{12}$, we go to Row 1 and Column 2 to read $-1$. Finally, slicing Row 2 of $A$ gives the horizontal $1 \times 3$ vector $\begin{pmatrix}0 & 4 & 5\end{pmatrix}$, and slicing Column 1 of $B$ gives the vertical $3 \times 1$ vector $\begin{pmatrix}1 \\ -2 \\ 4\end{pmatrix}$."*
