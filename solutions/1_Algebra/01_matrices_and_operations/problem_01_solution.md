### Exercise 1: Matrix Size and Entries

#### 1. Sizes of Matrices $A$ and $B$

* **Method / Definition:** The size (dimension) of a matrix is written as $m \times n$, where:
* $m$ = number of horizontal **rows**
* $n$ = number of vertical **columns**


* **Matrix $A$:**

$$A = \begin{pmatrix} 2 & -1 & 3 \\ 0 & 4 & 5 \end{pmatrix}$$



Counting rows and columns:
* Rows: 2 (Row 1: $\begin{pmatrix} 2 & -1 & 3 \end{pmatrix}$, Row 2: $\begin{pmatrix} 0 & 4 & 5 \end{pmatrix}$)
* Columns: 3
* **Result:** $A$ is of size **$2 \times 3$**.


* **Matrix $B$:**

$$B = \begin{pmatrix} 1 & 0 \\ -2 & 3 \\ 4 & 1 \end{pmatrix}$$



Counting rows and columns:
* Rows: 3
* Columns: 2
* **Result:** $B$ is of size **$3 \times 2$**.


* **Verification:** The total number of entries in an $m \times n$ matrix is $m \cdot n$.
* For $A$: $2 \times 3 = 6$ entries (matching the 6 numbers present).
* For $B$: $3 \times 2 = 6$ entries (matching the 6 numbers present).



---

#### 2. Reading Matrix Entries

* **Method / Definition:** The entry $m_{ij}$ denotes the element located at **row $i$** and **column $j$** of matrix $M$ (always "row first, column second").
* **Finding the entries:**
* **$a_{12}$:** Look at matrix $A$, Row 1, Column 2 $\to$ **$-1$**
* **$a_{23}$:** Look at matrix $A$, Row 2, Column 3 $\to$ **$5$**
* **$b_{21}$:** Look at matrix $B$, Row 2, Column 1 $\to$ **$-2$**
* **$b_{32}$:** Look at matrix $B$, Row 3, Column 2 $\to$ **$1$**


* **Result:**

$$a_{12} = -1, \quad a_{23} = 5, \quad b_{21} = -2, \quad b_{32} = 1$$



---

#### 3. Row and Column Vectors

* **Method / Definition:**
* A row is taken horizontally across the matrix. It can be written as a row vector $\begin{pmatrix} x_1 & x_2 & \dots & x_n \end{pmatrix}$ (size $1 \times n$).
* A column is taken vertically down the matrix. It can be written as a column vector $\begin{pmatrix} y_1 \\ y_2 \\ \dots \\ y_m \end{pmatrix}$ (size $m \times 1$).


* **Second row of $A$:**
* Take the entire second horizontal line of $A$:

$$\mathbf{r}_2(A) = \begin{pmatrix} 0 & 4 & 5 \end{pmatrix}$$



*(or as a standard coordinate vector $(0, 4, 5)$)*


* **First column of $B$:**
* Take the entire first vertical slice of $B$:

$$\mathbf{c}_1(B) = \begin{pmatrix} 1 \\ -2 \\ 4 \end{pmatrix}$$




* **Verification:**
* Row 2 of $A$ has length 3, which matches the number of columns in $A$ ($n = 3$).
* Column 1 of $B$ has height 3, which matches the number of rows in $B$ ($m = 3$).