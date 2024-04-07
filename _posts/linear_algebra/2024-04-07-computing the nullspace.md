---
layout: single
category: 선형대수
title: "computing the nullspace"
use_math: true
---
 ## Computing the Nullspace; N(A)

$$A = \begin{bmatrix} 1 & 2 & 2 & 2 \\ 2 & 4 & 6 & 8 \\ 3 & 6 & 8 & 10 \\ \end{bmatrix} \\ \to \begin{bmatrix} 1 & 2 & 2 & 2 \\ 0 & 0 & 2 & 4 \\ 0 & 0 & 2 & 4 \\ \end{bmatrix} \\ \to \begin{bmatrix} 1 & 2 & 2 & 2 \\ 0 & 0 & 2 & 4 \\ 0 & 0 & 0 & 0 \\ \end{bmatrix} $$

$Ax = 0 \leftrightarrow ux = 0$


elimination은 null space를 바꾸지 않는다. 

$pivot\ column = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}, \begin{bmatrix} 0 \\ 2 \\ 2 \end{bmatrix}$ 2개

$free\ column = \begin{bmatrix} 2 \\ 0 \\ 0 \end{bmatrix},\begin{bmatrix} 2 \\ 4 \\ 0 \end{bmatrix}$ 2개

rank of A = number of pivots = 2

## X
vector X에서 free column에 대응하는 2,4 행에는 임의의 수를 배정한다. 

$X = \begin{bmatrix} \Box \\ 1 \\ \Box \\ 0 \end{bmatrix}$

uX = 0 에서 $x_2 = 1, x_4 = 0$ 를 대입한다. 

$x_1 + 2x_2 + 2x_3 + 2x_4 = 0$ 

$0+0+ 2 x_3 + 4x_4 = 0$

식을 전개하면 $x_1 = -2, x_3 =0$ 임을 알수 있다. 따라서, 

$X = c\begin{bmatrix} -2 \\ 1 \\ 0 \\ 0 \end{bmatrix}$

또 다른 임의의 수를 free variable에 대입하여 $x_2 = 0, x_4 = 1$을 대입하면, 위와 같은 방법으로 $x_1 = 2, x_3 = -2$임을 알 수 있다.

$X = c\begin{bmatrix} 2 \\ 0 \\ -2 \\ 1\end{bmatrix}$

따라서, null space는 $X=c_1\begin{bmatrix} -2 \\ 1 \\ 0 \\0 \end{bmatrix} + c_2\begin{bmatrix} 2 \\ 0 \\ -2 \\ 1\end{bmatrix}$이다.

## Reduced Row Echelon Form(1)
$$ \begin{bmatrix} 1 & 2 & 2 & 2 \\ 0 & 0 & 2 & 4 \\ 0 & 0 & 0 & 0 \\ \end{bmatrix} \\ \to \begin{bmatrix} 1 & 2 & 0 & -2 \\ 0 & 0 & 2 & 4 \\ 0 & 0 & 0 & 0 \\ \end{bmatrix} \\ \to \begin{bmatrix} 1 & 2 & 0 & -2 \\ 0 & 0 & 1 & 2 \\ 0 & 0 & 0 & 0 \\ \end{bmatrix} = R = rref(A) $$
 
 (첫번째 시행) 1열에서 2열에서 뺀다. 

 (두번째 시행) 2열에 1/2를 곱한다.

- pivot : $R_{11}, R_{23}$
- pivot column: 1,3열
- pivot row: 1,2행

$\begin{bmatrix} 1 & 0 \\ 0 & 1 \\ \end{bmatrix} = I$가 pivot row와 pivot column 안에 있다. 

$\begin{bmatrix} 1 & 2 & 0 & -2 \\ 0 & 0 & 1 & 2 \\ 0 & 0 & 0 & 0 \\ \end{bmatrix}$를 pivot columns와 free columns로 나누어 표현하면, 

$\begin{bmatrix} 1 & 0 & 2 & -2 \\ 0 & 1 & 0 & 2 \\ 0 & 0 & 0 & 0 \\ \end{bmatrix}$ = $\begin{bmatrix} I & F  \\ 0 & 0  \\ \end{bmatrix}$

여기서 $F= \begin{bmatrix} 2 & -2 \\ 0 & 2 \\ \end{bmatrix}$는

$X=c_1\begin{bmatrix} -2 \\ 1 \\ 0 \\0 \end{bmatrix} + c_2\begin{bmatrix} 2 \\ 0 \\ -2 \\ 1\end{bmatrix}$의 free column에 대응하는 부분인 1행과 3행에서  $-F$ 형태로 나타난다. 

## Reduced Row Echelon Form(2)

$$Rx = 0$$

$$ \begin{bmatrix} I & F \end{bmatrix} \begin{bmatrix} x_{pivot} \\ x_{free} \end{bmatrix} = 0 $$

### null space matrix 

$$ RN = 0 $$
$$ N = \begin{bmatrix} -F \\ I \end{bmatrix}  $$

## $A^T$

$$A^T = \begin{bmatrix} 1 & 2 & 3  \\ 2 & 4 & 6 \\ 2 & 6 & 8 \\ 2 & 8 & 10  \end{bmatrix} \to  \begin{bmatrix} 1 & 2 & 3  \\ 0 & 2 & 2 \\ 0 & 0 & 0 \\ 0 & 0 & 0  \end{bmatrix}$$

- pivot : $R_{11}, R_{22}$
- rank of $A^T$ = num(pivots) = 2
- rank of A = rank of $A^T$ 

pivot column = 1,2열, free column = 3열

x = $\begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix}$

free variable $x_3 = 1$을 대입하면, 

$$ x= c\begin{bmatrix} -1 \\ -1 \\ 1 \end{bmatrix}$$

$$\begin{bmatrix} 1 & 2 & 3  \\ 0 & 2 & 2 \\ 0 & 0 & 0 \\ 0 & 0 & 0  \end{bmatrix} \to \begin{bmatrix} 1 & 0 & 1  \\ 0 & 1 & 1 \\ 0 & 0 & 0 \\ 0 & 0 & 0  \end{bmatrix} = \begin{bmatrix} I &  &F   \\  \\0 & 0 & 0 \\ 0 & 0 & 0  \end{bmatrix} $$

$$ x= c\begin{bmatrix} -1 \\ -1 \\ 1 \end{bmatrix} = c\begin{bmatrix} -F  \\ \\ I 
\\ \end{bmatrix}$$

null space matrix $N = \begin{bmatrix} -F  \\ \\ I \end{bmatrix} = \begin{bmatrix} -1 \\ -1 \\ 1 \end{bmatrix}$