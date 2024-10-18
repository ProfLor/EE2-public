---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.16.4
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---
(ref:Tutorial01)=
# Tutorial 01

## Repetition of Matrix Calculus

---

The purpose of this tutorial is to repeat basic matrix calculus operations. The following 2 x 2 matrices are provided in general form:
::::{grid}
:gutter: 4

:::{grid-item-card}
$$
M_1=
\begin{bmatrix}
A&B\\
C&D
\end{bmatrix}
$$
:::

:::{grid-item-card}
$$
M_2=
\begin{bmatrix}
E&F\\
G&H
\end{bmatrix}
$$
:::

:::{grid-item-card}
$$
M_3=
\begin{bmatrix}
I&J\\
K&L
\end{bmatrix}
$$
:::

:::{grid-item-card}
$$
M_4=
\begin{bmatrix}
D&-B\\
-C&A
\end{bmatrix}
$$
:::
::::

### Exercise 1: Matrix addition

1. Calculate the sum  $M_2+M_3$ and the difference  $M_2-M_3$.

    ```{toggle}
    > $$
    M_2+M_3=
    \begin{bmatrix}
    E+I&F+J\\
    G+K&H+L
    \end{bmatrix}
    $$
    ```

    ```{toggle}
    > $$M_2-M_3=
    \begin{bmatrix}
    E-I&F-J\\
    G-K&H-L
    \end{bmatrix}
    $$
    ```

1. Calculate the sum $M_1+M_4$ and the difference $M_1-M_4$.

    ```{toggle}
    > $$
    M_1+M_4=
    \begin{bmatrix}
    A+D&0\\
    0&D+A
    \end{bmatrix}
    $$
    ```

    ```{toggle}
    > $$
    M_1-M_4=
    \begin{bmatrix}
    A-D&2 B\\
    2 C&D-A
    \end{bmatrix}
    $$
    ```

### Exercise 2: Matrix multiplication

1. Calculate the determinants of all matrices ${M_1}$, ${M_2}$, ${M_3}$ and ${M_4}$.

    ```{toggle}
    > $$
    \begin{align*}
    \det{M_1} &= A \cdot D - B \cdot C \\
    \det{M_2} &= E \cdot H - F \cdot G \\
    \det{M_3} &= I \cdot L - J \cdot K \\
    \det{M_4} &= D \cdot A + B \cdot C
    \end{align*}
    $$
    ```

1. Calculate the products $M_1\cdot M_2$, $M_1\cdot M_3$, $M_2\cdot M_3$, $M_3\cdot M_2$, $M_1\cdot M_4$ and $M_4\cdot M_1$.

    ```{toggle}
    > $$
    M_1\cdot M_2=
    \begin{bmatrix}
    A \cdot E + B \cdot G & A \cdot F + B \cdot H \\
    C \cdot E + D \cdot G & C \cdot F + D \cdot H
    \end{bmatrix}
    $$
    ```

    ```{toggle}
    > $$M_1 \cdot M_3 =
    \begin{bmatrix}
    A \cdot I + B \cdot K & A \cdot J + B \cdot L \\
    C \cdot I + D \cdot K & C \cdot J + D \cdot L
    \end{bmatrix}
    $$
    ```

    ```{toggle}
    > $$
    M_2 \cdot M_3 =
    \begin{bmatrix}
    E \cdot I + F \cdot K & E \cdot J + F \cdot L \\
    G \cdot I + H \cdot K & G \cdot J + H \cdot L
    \end{bmatrix}
    $$
    ```

    ```{toggle}
    > $$
    M_3 \cdot M_2 =
    \begin{bmatrix}
    E \cdot I + G \cdot J & F \cdot I + H \cdot J \\
    E \cdot K + G \cdot L & F \cdot K + H \cdot L
    \end{bmatrix}
    $$
    ```

    ```{toggle}
    > $$
    M_1 \cdot M_4 =
    \begin{bmatrix}
    A \cdot D - B \cdot C & 0 \\
    0 & A \cdot D - B \cdot C
    \end{bmatrix}
    = \det M_1 \cdot
    \begin{bmatrix}
    1 & 0 \\
    0 & 1
    \end{bmatrix}
    $$
    ```

    ```{toggle}
    > $$
    M_4 \cdot M_1 =
    \begin{bmatrix}
    A \cdot D - B \cdot C & 0 \\
    0 & A \cdot D - B \cdot C
    \end{bmatrix}
    = \det M_4 \cdot
    \begin{bmatrix}
    1 & 0 \\
    0 & 1
    \end{bmatrix}
    $$
    ```

1. Compare the two products $\left(M_1\cdot M_2\right)\cdot M_3$ and $M_1\cdot \left(M_2\cdot M_3\right)$.

    ```{toggle}
    > $$
    \left(M_1\cdot M_2\right)\cdot M_3\\
    =
    \begin{bmatrix}
    A \cdot E + B \cdot G & A \cdot F + B \cdot H \\
    C \cdot E + D \cdot G & C \cdot F + D \cdot H
    \end{bmatrix}
    \cdot
    \begin{bmatrix}
    I & J \\
    K & L
    \end{bmatrix} \\
    =
    \begin{bmatrix}
    A \cdot E \cdot I + A \cdot F \cdot K + B \cdot G \cdot I + B \cdot H \cdot K & A \cdot E \cdot J + A \cdot F \cdot L + B \cdot G \cdot J + B \cdot H \cdot L \\
    C \cdot E \cdot I + C \cdot F \cdot K + D \cdot G \cdot I + D \cdot H \cdot K & C \cdot E \cdot J + C \cdot F \cdot L + D \cdot G \cdot J + D \cdot H \cdot L
    \end{bmatrix}
    $$
    ```

    ```{toggle}
    > $$
    M_1\cdot \left(M_2\cdot M_3\right)\\
    =
    \begin{bmatrix}
    A & B \\
    C & D
    \end{bmatrix}
    \cdot
    \begin{bmatrix}
    E \cdot I + F \cdot K & E \cdot J + F \cdot L \\
    G \cdot I + H \cdot K & G \cdot J + H \cdot L
    \end{bmatrix} \\
    =
    \begin{bmatrix}
    A \cdot E \cdot I + B \cdot G \cdot I + A \cdot F \cdot K + B \cdot H \cdot K & A \cdot E \cdot J + B \cdot G \cdot J + A \cdot F \cdot L + B \cdot H \cdot L \\
    C \cdot E \cdot I + D \cdot G \cdot I + C \cdot F \cdot K + D \cdot H \cdot K & C \cdot E \cdot J + D \cdot G \cdot J + C \cdot F \cdot L + D \cdot H \cdot L
    \end{bmatrix}
    $$
    ```

### Exercise 3: Matrix inversion

1. For all four matrices $M_1$ to $M_4$: calculate the inverse matrices $M_1^{-1}$ to $M_4^{-1}$.

    ```{toggle}
    > $$
    M_1^{-1}=
    \frac{1}{\det{M_1}}
    \begin{bmatrix}
    D&-B\\
    -C&A
    \end{bmatrix}
    $$
    ```{toggle}
    > $$
    M_2^{-1}=
    \frac{1}{\det{M_2}}
    \begin{bmatrix}
    H&-F\\
    -G&E
    \end{bmatrix}
    $$
    ```{toggle}
    > $$
    M_3^{-1}=
    \frac{1}{\det{M_3}}
    \begin{bmatrix}
    L&-J\\
    -K&I
    \end{bmatrix}
    $$
    ```{toggle}
    > $$
    > M_4^{-1}=
    > \frac{1}{\det{M_4}}
    > \begin{bmatrix}
    > A&-B\\
    > -C&D
    > \end{bmatrix}
    $$
    ```

    (ref:Exercise032)=
1. What are the results of $M_1\cdot M_1^{-1}$ and $M_1^{-1}\cdot M_1$?

    ```{toggle}
    > $$
    M_1\cdot M_1^{-1}=
    \frac{1}{\det{M_1}}
    \begin{bmatrix}
    A\cdot D-B\cdot C&0\\
    0&A\cdot D-B\cdot C
    \end{bmatrix}
    =
    \begin{bmatrix}
    1&0\\
    0&1
    \end{bmatrix}
    $$
    ```

    ```{toggle}
    > $$
    M_1^{-1}\cdot M_1=
    \frac{1}{\det{M_1}}
    \begin{bmatrix}
    A \cdot D - B \cdot C & 0\\
    0 & A \cdot D - B \cdot C
    \end{bmatrix}
    =
    \begin{bmatrix}
    1 & 0\\
    0 & 1
    \end{bmatrix}
    $$
    ```

1. What is the term for the type of matrix you calculated in [exercise 3.2](ref:Exercise032)?

    ```{toggle}
    > The matrix is called the identity matrix.
    ````

### Exercise 4: Equation systems

1. What are the results of the following multiplication operations?
    ::::{grid}
    :gutter: 3

    :::{grid-item-card}
    $$
    \begin{bmatrix}
    A&B\\\
    C&D
    \end{bmatrix}
    \cdot
    \begin{bmatrix}
    X\\Y
    \end{bmatrix}
    $$
    :::

    :::{grid-item-card}
    $$
    \begin{bmatrix}
    R_1+R_2&R_2\\
    R_2&R_2+R_3
    \end{bmatrix}
    \cdot
    \begin{bmatrix}
    I_1\\
    I_2
    \end{bmatrix}
    $$
    :::

    :::{grid-item-card}
    $$
    \begin{bmatrix}
    G_1+G_2&-G_1\\
    -G_2&G_2+G_3
    \end{bmatrix}
    \cdot
    \begin{bmatrix}
    U_1\\
    U_2
    \end{bmatrix}
    $$
    :::
    ::::

    ```{toggle}
    > $$
    \begin{bmatrix}
        A&B\\\
        C&D
        \end{bmatrix}
        \cdot
        \begin{bmatrix}
        X\\Y
        \end{bmatrix}
        =
    \begin{bmatrix}
    A\cdot X+B\cdot Y\\
    C\cdot X+D\cdot Y
    \end{bmatrix}
    $$
    ```

   ```{toggle}
    > $$
    \begin{bmatrix}
        R_1+R_2&R_2\\
        R_2&R_2+R_3
        \end{bmatrix}
        \cdot
        \begin{bmatrix}
        I_1\\
        I_2
        \end{bmatrix}
        =
    \begin{bmatrix}
    \left(R_1+R_2\right)\cdot I_1& R_2\cdot I_2\\
    R_2\cdot I_1&\left(R_2+R_3\right)\cdot I_2
    \end{bmatrix}
    $$
    ```

    ```{toggle}
    > $$
    \begin{bmatrix}
        G_1+G_2&-G_1\\
        -G_2&G_2+G_3
        \end{bmatrix}
        \cdot
        \begin{bmatrix}
        U_1\\
        U_2
        \end{bmatrix}
        =
    \begin{bmatrix}
    \left(G_1+G_2\right)\cdot U_1-G_1\cdot U_2\\
    -G_2\cdot U_1+\left(G_2+G_3\right)\cdot U_2
    \end{bmatrix}
    $$
    ```
    (ref:ex42)=
1. Please expand the following equation systems into ordinary equations:
    ::::{grid}
    :gutter: 2

    :::{grid-item-card}
   $$
    \begin{bmatrix}
    U_1\\U_2
    \end{bmatrix}
    =
    \begin{bmatrix}
    R_1+R_2&R_2\\
    R_2&R_2
    \end{bmatrix}
    \cdot
    \begin{bmatrix}
    I_1\\
    I_2
    \end{bmatrix}
    $$
    :::

    :::{grid-item-card}
    $$
    \begin{bmatrix}
    I_1\\
    I_2
    \end{bmatrix}
    =
    \begin{bmatrix}
    G_1&-G_1\\
    -G_1&G_1+G_2
    \end{bmatrix}
    \cdot
    \begin{bmatrix}
    U_1\\
    U_2
    \end{bmatrix}
    $$
    :::
    ```{toggle}
    > $$
    \begin{align*}
    U_1&=\left(R_1+ R_2\right)\cdot I_1+R_2\cdot I_2\\
    U_2&=R_2\cdot I_1+R_2\cdot I_2
    \end{align*}
    $$
    ```

    ```{toggle}
    > $$
    \begin{align*} 
    I_1&=G_1\cdot U_1-G_1\cdot U_2\\
    I_2&=-G_1\cdot U_1+\left(G_1+G_2\right)\cdot U_2
    \end{align*}
    $$
    ```

1. Write the following equations in matrix notation. The voltages U1 and U2 and the currents I1 and I2 should be represented as column vectors which are connected by a resistance or an admittance matrix (see [exercise 4.2](ref:ex42)):
     ::::{grid}
    :gutter: 2

    :::{grid-item-card}
    $$
    \begin{align*}
    U_1&=R_1\cdot I_1+R_2\cdot I_1+R_2\cdot I_2\\
    U_2&=R_2\cdot I_2+R_3\cdot I_2+R_2\cdot I_1 &
    \end{align*}
    $$
    :::

    :::{grid-item-card}
    $$
    \begin{align*}
    I_1&=G_1\cdot U_1+G_2\cdot \left(U_1-U_2\right)\\
    I_2&=G_3\cdot U_2+G_2\cdot \left( U_2- U_1\right)
    \end{align*}
    $$
    :::

    ```{toggle}
    > $$
    \begin{bmatrix}
    U_1\\
    U_2
    \end{bmatrix}
    =
    \begin{bmatrix}
    R_1+R_2&R_2\\
    R_2&R_2+R_3
    \end{bmatrix}
    \cdot
    \begin{bmatrix}
    I_1\\
    I_2
    \end{bmatrix}
    ```

    ```{toggle}
    \begin{bmatrix}
    I_1\\
    I_2
    \end{bmatrix}
    =
    \begin{bmatrix}
    G_1+G_2&-G_2\\
    -G_1&G_2+G_3
    \end{bmatrix}
    \cdot
    \begin{bmatrix}
    U_1\\
    U_2
    \end{bmatrix}
    $$
    ```

1. Invert the resistance matrix and the admittance matrix of [exercise 4.2](ref:ex42):
    ::::{grid}
    :gutter: 2

    :::{grid-item-card}
    $$
    \begin{bmatrix}
    R_1+R_2&R_2\\
    R_2&R_2
    \end{bmatrix}^{-1}
    $$
    :::

    :::{grid-item-card}
    $$
    \begin{bmatrix}
    G_1&-G_1\\
    -G_1&G_1+G_2
    \end{bmatrix}^{-1}
    $$
    :::

    ```{toggle}
    > $$
     \begin{bmatrix}
    R_1+R_2&R_2\\
    R_2&R_2
    \end{bmatrix}^{-1}
    =
    \frac{1}{R_1\cdot R_2}
    \begin{bmatrix}
    R_2&-R_2\\
    -R_2&R_1+R_2
    \end{bmatrix}
    =
    \begin{bmatrix}
    G_1 &-G_1\\
    -G_1&G_1+G_2
    \end{bmatrix}
    $$
    ```

    ```{toggle}
    > $$
    \begin{bmatrix}
    G_1&-G_1\\
    -G_1&G_1+G_2
    \end{bmatrix}^{-1}
    =
    \frac{1}{G_1\cdot G_2}
    \begin{bmatrix}
    G_1+G_2&G_1\\
    G_1&G_1
    \end{bmatrix}
    =
    \begin{bmatrix}
    R_1+R_2&R_2\\
    R_2&R_2
    \end{bmatrix}
    $$
    ```

1. Compare the inverse resistance matrix with the original admittance matrix, and the inverse admittance matrix with the original resistance matrix.

    ```{toggle}
    >The inverse resistance matrix is the same as the original conductance matrix, and the inverse conductance matrix is the same as the original resistance matrix.
    ```
