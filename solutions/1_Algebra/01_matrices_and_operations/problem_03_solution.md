# Exercise 3: When Can Matrices Be Multiplied?

## 1. Problem Statement

Given matrices with the following sizes:

$$
A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}
$$

For each of the eight products:

$$
AB,\quad BA,\quad BC,\quad CB,\quad AC,\quad CA,\quad AD,\quad DA
$$

1. Determine whether the product is **defined** (possible) or **undefined** (impossible).
2. If defined, state the **size of the resulting matrix**.
3. Justify each decision using the **dimension compatibility condition**.

---

## 2. Theoretical Background and Concepts

### How Does Matrix Multiplication Work?
Unlike matrix addition (which is just adding numbers in matching spots), matrix multiplication works by taking **rows of the first matrix** and multiplying them by **columns of the second matrix** (the "Row-by-Column" rule or dot product).

To compute a single entry in row $i$ and column $j$ of the product $XY$:
* You take **Row $i$** from the first matrix $X$.
* You take **Column $j$** from the second matrix $Y$.
* You multiply their matching numbers and add them all together:
  $$
  (XY)_{ij} = x_{i1}y_{1j} + x_{i2}y_{2j} + \dots + x_{ik}y_{kj}
  $$

### The Dimension Compatibility Condition (The "Inner Match" Rule)
For this "Row-by-Column" pairing to work, **the length of a row in the first matrix must equal the height of a column in the second matrix**:
* The length of a row in $X$ is the **number of columns** of $X$.
* The height of a column in $Y$ is the **number of rows** of $Y$.

If $X$ has size $m \times k$ and $Y$ has size $p \times n$:

$$
X_{\mathbf{m} \times \mathbf{\color{blue}k}} \cdot Y_{\mathbf{\color{blue}p} \times \mathbf{n}}
$$

1. **Compatibility Condition:** The multiplication $XY$ is defined if and only if the **inner dimensions are equal**:
   $$
   k = p
   $$
   *(Columns of First = Rows of Second)*
2. **Resulting Size:** If they match, the **outer dimensions** determine the size of the product:
   $$
   \text{Size of } XY = m \times n
   $$

> **Simple Analogy (Plugging in a Cable):**
> Think of the first matrix having $k$ output pins and the second matrix having $p$ input holes. They can only plug together if the number of pins matches the number of holes ($k = p$). The resulting device has the input format of the first ($m$) and the output format of the second ($n$).

### Noncommutativity of Multiplication
With regular numbers, order does not matter: $3 \times 5 = 5 \times 3 = 15$.
With matrices, **order matters completely**:
* $AB$ might be defined, while $BA$ is completely undefined.
* Even if both are defined, they often have completely different sizes or produce different matrices ($AB \neq BA$).

---

## 3. Detailed Step-by-Step Analysis

We examine each of the eight given products one by one:

---

### 1. Product $AB$
* **Dimensions:** $A_{2 \times \mathbf{3}}$ and $B_{\mathbf{3} \times 4}$.
* **Compatibility Check:**
  * Columns of $A = 3$
  * Rows of $B = 3$
  * Inner numbers match: $3 = 3$.
* **Conclusion:**
  $$
  \boxed{AB \text{ is \textbf{defined}}, \quad \text{Size} = 2 \times 4}
  $$
* **Justification:** The number of columns in $A$ (3) equals the number of rows in $B$ (3). The resulting size is formed by the outer dimensions: $2$ rows and $4$ columns.

---

### 2. Product $BA$
* **Dimensions:** $B_{3 \times \mathbf{4}}$ and $A_{\mathbf{2} \times 3}$.
* **Compatibility Check:**
  * Columns of $B = 4$
  * Rows of $A = 2$
  * Inner numbers do not match: $4 \neq 2$.
* **Conclusion:**
  $$
  \boxed{BA \text{ is \textbf{undefined}}}
  $$
* **Justification:** A row of $B$ contains 4 entries, but a column of $A$ contains only 2 entries. Because their lengths differ, the row-column dot product cannot be computed.

---

### 3. Product $BC$
* **Dimensions:** $B_{3 \times \mathbf{4}}$ and $C_{\mathbf{4} \times 2}$.
* **Compatibility Check:**
  * Columns of $B = 4$
  * Rows of $C = 4$
  * Inner numbers match: $4 = 4$.
* **Conclusion:**
  $$
  \boxed{BC \text{ is \textbf{defined}}, \quad \text{Size} = 3 \times 2}
  $$
* **Justification:** The number of columns in $B$ (4) equals the number of rows in $C$ (4). The outer dimensions yield a $3 \times 2$ matrix.

---

### 4. Product $CB$
* **Dimensions:** $C_{4 \times \mathbf{2}}$ and $B_{\mathbf{3} \times 4}$.
* **Compatibility Check:**
  * Columns of $C = 2$
  * Rows of $B = 3$
  * Inner numbers do not match: $2 \neq 3$.
* **Conclusion:**
  $$
  \boxed{CB \text{ is \textbf{undefined}}}
  $$
* **Justification:** The number of columns in $C$ (2) does not match the number of rows in $B$ (3).

---

### 5. Product $AC$
* **Dimensions:** $A_{2 \times \mathbf{3}}$ and $C_{\mathbf{4} \times 2}$.
* **Compatibility Check:**
  * Columns of $A = 3$
  * Rows of $C = 4$
  * Inner numbers do not match: $3 \neq 4$.
* **Conclusion:**
  $$
  \boxed{AC \text{ is \textbf{undefined}}}
  $$
* **Justification:** Rows of $A$ have 3 entries, while columns of $C$ have 4 entries ($3 \neq 4$), making multiplication impossible.

---

### 6. Product $CA$
* **Dimensions:** $C_{4 \times \mathbf{2}}$ and $A_{\mathbf{2} \times 3}$.
* **Compatibility Check:**
  * Columns of $C = 2$
  * Rows of $A = 2$
  * Inner numbers match: $2 = 2$.
* **Conclusion:**
  $$
  \boxed{CA \text{ is \textbf{defined}}, \quad \text{Size} = 4 \times 3}
  $$
* **Justification:** The number of columns in $C$ (2) equals the number of rows in $A$ (2). The outer dimensions yield a $4 \times 3$ matrix.

---

### 7. Product $AD$
* **Dimensions:** $A_{2 \times \mathbf{3}}$ and $D_{\mathbf{2} \times 2}$.
* **Compatibility Check:**
  * Columns of $A = 3$
  * Rows of $D = 2$
  * Inner numbers do not match: $3 \neq 2$.
* **Conclusion:**
  $$
  \boxed{AD \text{ is \textbf{undefined}}}
  $$
* **Justification:** Matrix $A$ has 3 columns, but matrix $D$ has only 2 rows ($3 \neq 2$).

---

### 8. Product $DA$
* **Dimensions:** $D_{2 \times \mathbf{2}}$ and $A_{\mathbf{2} \times 3}$.
* **Compatibility Check:**
  * Columns of $D = 2$
  * Rows of $A = 2$
  * Inner numbers match: $2 = 2$.
* **Conclusion:**
  $$
  \boxed{DA \text{ is \textbf{defined}}, \quad \text{Size} = 2 \times 3}
  $$
* **Justification:** The number of columns in $D$ (2) equals the number of rows in $A$ (2). The outer dimensions yield a $2 \times 3$ matrix.

---

## 4. Summary Table and Consistency Checks

### Complete Summary Table

| Product | First Matrix ($X$) | Second Matrix ($Y$) | Inner Condition ($c_X = r_Y$) | Status | Resulting Size ($r_X \times c_Y$) |
| :---: | :---: | :---: | :---: | :---: | :---: |
| **$AB$** | $2 \times 3$ | $3 \times 4$ | $3 = 3$ | **Defined** | $\mathbf{2 \times 4}$ |
| **$BA$** | $3 \times 4$ | $2 \times 3$ | $4 \neq 2$ | **Undefined** | — |
| **$BC$** | $3 \times 4$ | $4 \times 2$ | $4 = 4$ | **Defined** | $\mathbf{3 \times 2}$ |
| **$CB$** | $4 \times 2$ | $3 \times 4$ | $2 \neq 3$ | **Undefined** | — |
| **$AC$** | $2 \times 3$ | $4 \times 2$ | $3 \neq 4$ | **Undefined** | — |
| **$CA$** | $4 \times 2$ | $2 \times 3$ | $2 = 2$ | **Defined** | $\mathbf{4 \times 3}$ |
| **$AD$** | $2 \times 3$ | $2 \times 2$ | $3 \neq 2$ | **Undefined** | — |
| **$DA$** | $2 \times 2$ | $2 \times 3$ | $2 = 2$ | **Defined** | $\mathbf{2 \times 3}$ |

### Associativity Consistency Check (Multi-Matrix Chain)
Notice that we can chain the defined products $A(BC)$ and $(AB)C$:
* **Route 1: $A(BC)$**
  * $BC$ has size $3 \times 2$.
  * Multiplying $A_{2 \times 3}$ by $(BC)_{3 \times 2}$: inner dimensions match ($3 = 3$), resulting in a **$2 \times 2$** matrix.
* **Route 2: $(AB)C$**
  * $AB$ has size $2 \times 4$.
  * Multiplying $(AB)_{2 \times 4}$ by $C_{4 \times 2}$: inner dimensions match ($4 = 4$), resulting in a **$2 \times 2$** matrix.
* Both routes give identical dimensions ($2 \times 2$), confirming that our individual size derivations are consistent with matrix associativity $(AB)C = A(BC)$.

---

## 5. Common Mistakes to Avoid

1. **Assuming Commutativity:**
   * Assuming that if $AB$ is defined, $BA$ must also be defined. As shown above, $AB$ is defined ($2 \times 4$), but $BA$ is completely undefined ($4 \neq 2$).
2. **Confusing Inner vs. Outer Dimensions:**
   * The **inner** dimensions determine whether multiplication is legal ($c_1 = r_2$).
   * The **outer** dimensions determine the resulting size ($r_1 \times c_2$).
3. **Comparing Total Entries Instead of Compatible Dimensions:**
   * Matrix multiplication is not about whether two matrices have the same number of total numbers. It depends strictly on matching row-length with column-height.

---

## 6. How I Would Explain This in Class (Oral Summary)

> *"To determine if two matrices can be multiplied, we check the dimension compatibility condition: the number of columns in the first matrix must equal the number of rows in the second. In notation $(m \times k) \times (p \times n)$, the inner numbers must match ($k = p$), and the outer numbers give the new size $(m \times n)$. Out of the eight pairs, four are defined ($AB$ is $2 \times 4$, $BC$ is $3 \times 2$, $CA$ is $4 \times 3$, and $DA$ is $2 \times 3$), while the other four ($BA$, $CB$, $AC$, and $AD$) are undefined because their inner dimensions do not match. This also clearly demonstrates that matrix multiplication is non-commutative: $AB$ exists, but $BA$ does not."*

