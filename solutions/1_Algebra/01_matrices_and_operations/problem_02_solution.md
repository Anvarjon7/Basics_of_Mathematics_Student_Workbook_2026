# Exercise 2: Addition and Scalar Multiplication

## 1. Problem Statement

Given the matrices:

$$
A = \begin{pmatrix}
1 & 2 \\
-1 & 3
\end{pmatrix},
\qquad
B = \begin{pmatrix}
4 & -2 \\
0 & 5
\end{pmatrix}
$$

1. Compute $A + B$.
2. Compute $A - B$.
3. Compute $3A - 2B$.
4. Explain why matrix addition is possible only for matrices of the same size.

---

## 2. Theoretical Background and Concepts

### What is Matrix Addition?
Matrix addition is **entry-by-entry** (or componentwise) addition.
Think of two ice cube trays or egg cartons with matching compartments:
* You take the number in the top-left slot of the first tray, and add it to the number in the top-left slot of the second tray.
* You repeat this for every single slot in the grid.

Formally, if $C = A + B$, then each entry $c_{ij}$ is given by:
$$
c_{ij} = a_{ij} + b_{ij}
$$

### What is Matrix Subtraction?
Subtraction works the exact same way as addition, but you subtract matching slots:
$$
(A - B)_{ij} = a_{ij} - b_{ij}
$$
> **Watch the Signs:** When subtracting a negative number, remember that minus a minus becomes a plus: $x - (-y) = x + y$.

### What is Scalar Multiplication?
In linear algebra, a **scalar** is simply an ordinary single number (like $3$, $-2$, or $0.5$).
To multiply a matrix by a scalar $k$, you multiply **every single number inside the matrix** by $k$:
$$
(kA)_{ij} = k \cdot a_{ij}
$$

### Why Must Sizes Match?
To add or subtract two matrices, they **must have the exact same size** ($m \times n$).
* Every entry in $A$ needs a corresponding "partner" in $B$ located at the exact same row and column.
* If one matrix is $2 \times 2$ and another is $2 \times 3$, the entries in the third column would have nothing to add to. You cannot add an empty space to a number.

---

## 3. Detailed Step-by-Step Solution

### Step 1: Check Dimensions
* Matrix $A$ has 2 rows and 2 columns $\implies \text{size } 2 \times 2$.
* Matrix $B$ has 2 rows and 2 columns $\implies \text{size } 2 \times 2$.

Since both matrices have the identical size ($2 \times 2$), addition, subtraction, and linear combinations are all well-defined, and the resulting matrices will also be of size $2 \times 2$.

---

### Step 2: Compute $A + B$

Add corresponding entries located at each coordinate $(i, j)$:

$$
A + B = \begin{pmatrix}
1 & 2 \\
-1 & 3
\end{pmatrix}
+
\begin{pmatrix}
4 & -2 \\
0 & 5
\end{pmatrix}
=
\begin{pmatrix}
1 + 4 & 2 + (-2) \\
-1 + 0 & 3 + 5
\end{pmatrix}
$$

* **Row 1, Column 1:** $1 + 4 = 5$
* **Row 1, Column 2:** $2 + (-2) = 2 - 2 = 0$
* **Row 2, Column 1:** $-1 + 0 = -1$
* **Row 2, Column 2:** $3 + 5 = 8$

$$
\boxed{A + B = \begin{pmatrix}
5 & 0 \\
-1 & 8
\end{pmatrix}}
$$

---

### Step 3: Compute $A - B$

Subtract each entry of $B$ from the matching entry of $A$:

$$
A - B = \begin{pmatrix}
1 & 2 \\
-1 & 3
\end{pmatrix}
-
\begin{pmatrix}
4 & -2 \\
0 & 5
\end{pmatrix}
=
\begin{pmatrix}
1 - 4 & 2 - (-2) \\
-1 - 0 & 3 - 5
\end{pmatrix}
$$

* **Row 1, Column 1:** $1 - 4 = -3$
* **Row 1, Column 2:** $2 - (-2) = 2 + 2 = 4$
* **Row 2, Column 1:** $-1 - 0 = -1$
* **Row 2, Column 2:** $3 - 5 = -2$

$$
\boxed{A - B = \begin{pmatrix}
-3 & 4 \\
-1 & -2
\end{pmatrix}}
$$

---

### Step 4: Compute $3A - 2B$

We calculate the two scalar multiples first, and then subtract.

1. **Calculate $3A$:** Multiply every entry of $A$ by $3$:
   $$
   3A = 3 \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix}
   = \begin{pmatrix} 3 \cdot 1 & 3 \cdot 2 \\ 3 \cdot (-1) & 3 \cdot 3 \end{pmatrix}
   = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}
   $$

2. **Calculate $2B$:** Multiply every entry of $B$ by $2$:
   $$
   2B = 2 \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}
   = \begin{pmatrix} 2 \cdot 4 & 2 \cdot (-2) \\ 2 \cdot 0 & 2 \cdot 5 \end{pmatrix}
   = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}
   $$

3. **Subtract $2B$ from $3A$:**
   $$
   3A - 2B = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}
   - \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}
   = \begin{pmatrix} 3 - 8 & 6 - (-4) \\ -3 - 0 & 9 - 10 \end{pmatrix}
   $$

   * **Row 1, Column 1:** $3 - 8 = -5$
   * **Row 1, Column 2:** $6 - (-4) = 6 + 4 = 10$
   * **Row 2, Column 1:** $-3 - 0 = -3$
   * **Row 2, Column 2:** $9 - 10 = -1$

$$
\boxed{3A - 2B = \begin{pmatrix}
-5 & 10 \\
-3 & -1
\end{pmatrix}}
$$

---

### Step 5: Why Matrix Addition is Only Possible for Same-Size Matrices

1. **Definition by Pairing:** Matrix addition is strictly defined componentwise:
   $$(A + B)_{ij} = a_{ij} + b_{ij}$$
   This requires an exact one-to-one pairing between every entry $a_{ij}$ in $A$ and every entry $b_{ij}$ in $B$.
2. **Missing Partners:** If matrix $A$ has dimensions $m \times n$ and matrix $B$ has dimensions $p \times q$ with either $m \neq p$ or $n \neq q$, there will be positions $(i, j)$ that exist in one matrix but not in the other. Since adding a number to a non-existent entry is undefined in arithmetic, the sum cannot be formed.
3. **Geometric Interpretation:** Matrices of a fixed size $m \times n$ form a vector space $\mathbb{R}^{m \times n}$. Matrices of different sizes belong to entirely different vector spaces and therefore cannot be added together.

---

## 4. Verification and Consistency Checks

We can verify our calculations using standard algebraic matrix identities:

1. **Check via sum of $(A+B)$ and $(A-B)$:**
   Notice that $(A + B) + (A - B) = 2A$. Let's test our answers:
   $$
   \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}
   +
   \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}
   =
   \begin{pmatrix} 5 + (-3) & 0 + 4 \\ -1 + (-1) & 8 + (-2) \end{pmatrix}
   =
   \begin{pmatrix} 2 & 4 \\ -2 & 6 \end{pmatrix}
   $$
   Comparing with $2A$:
   $$
   2A = 2 \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} = \begin{pmatrix} 2 & 4 \\ -2 & 6 \end{pmatrix} \quad \checkmark
   $$

2. **Check via difference of $(A+B)$ and $(A-B)$:**
   Notice that $(A + B) - (A - B) = 2B$. Let's test our answers:
   $$
   \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}
   -
   \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}
   =
   \begin{pmatrix} 5 - (-3) & 0 - 4 \\ -1 - (-1) & 8 - (-2) \end{pmatrix}
   =
   \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}
   $$
   Comparing with $2B$:
   $$
   2B = 2 \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix} \quad \checkmark
   $$

3. **Check for $3A - 2B$ using an alternate route:**
   We can rewrite $3A - 2B$ as $3(A - B) + B$:
   $$
   3(A - B) + B = 3 \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix} + \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}
   = \begin{pmatrix} -9 & 12 \\ -3 & -6 \end{pmatrix} + \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}
   = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix} \quad \checkmark
   $$
   All three checks confirm the results are completely correct.

---

## 5. Common Mistakes to Avoid

1. **Sign Errors with Negatives:**
   * In $A - B$, the $(1, 2)$ entry is $2 - (-2) = 2 + 2 = 4$. A frequent mistake is writing $2 - 2 = 0$.
   * In $3A - 2B$, the $(1, 2)$ entry is $6 - (-4) = 6 + 4 = 10$.
2. **Partial Scalar Multiplication:**
   * Multiplying only the first row or first column by the scalar instead of every single entry in the matrix.
3. **Attempting to Add Different Dimensions:**
   * Trying to add a $2 \times 2$ matrix to a $2 \times 3$ matrix by "filling with zeros" without an explicit definition. Matrix addition is only defined when sizes match exactly.

---

## 6. How I Would Explain This in Class (Oral Summary)

> *"Matrix addition and subtraction are done entry-by-entry, which means we simply add or subtract numbers that sit in the exact same row and column position. Because of this position-by-position rule, both matrices must have the exact same dimensions—otherwise, some numbers would have no partner to pair with. For scalar multiplication, like $3A$, we multiply every entry inside $A$ by $3$. Combining these operations, we find $A+B = \begin{pmatrix}5 & 0 \\ -1 & 8\end{pmatrix}$, $A-B = \begin{pmatrix}-3 & 4 \\ -1 & -2\end{pmatrix}$, and $3A-2B = \begin{pmatrix}-5 & 10 \\ -3 & -1\end{pmatrix}$, which we confirmed using the identity $(A+B)+(A-B)=2A$."*

