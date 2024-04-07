---
layout: single
category: 선형대수
title: "Permutation Matrix"
use_math: true
---
## Recall: col picture & row picture
### col picture

$$ \begin {bmatrix}
| & | &|\\
col 1 & col 2 & col 3 \\
| & | &|\\
\end{bmatrix} \begin {bmatrix} 3\\4\\5 \end{bmatrix} = 3 col1 +4col + 5col3 $$

### row picture

$$\begin {bmatrix} 1\\2\\7 \end{bmatrix} \begin{bmatrix} -row1- \\ -row2- \\ -row3- \end{bmatrix} = 1row1 + 2row2 + 7row3$$ 

- row picture -> left multiplication
-  col picture -> right multiplication

## Matrix Multiplication
$$\begin {bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \begin {bmatrix} 1 & 2 & 1 \\ 3 & 8 & 1 \\ 0 & 4 & 1 \end{bmatrix} = \begin {bmatrix} 1 & 2 & 1 \\ 3 & 8 & 1 \\ 0 & 4 & 1 \end{bmatrix}$$

matrix를 row 측면에서 볼 때, 첫 번째 행에 첫번째 행이, 두 번째 행에 두 번째 행이, 세 번째 행에 세 번째 행이 온다고 해석할 수 있다. 

### STEP 1: $row2 - 3*row1$

$$E_{21}A = \begin {bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}\begin {bmatrix} 1 & 2 & 1 \\ 3 & 8 & 1 \\ 0 & 4 & 1 \end{bmatrix}\\= \begin {bmatrix} 1 & 2 & 1 \\ 0 & 2 & -2 \\ 0 & 4 & 1 \end{bmatrix}$$

첫번째 행에 첫번째 행이,
두번째 행에 $row2 - 3*row1$,
세번째 행에 세번째 행이 온다.

### STEP 2: $row3 - 2*row2$

$$E_{32}A' = \begin {bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & -2 & 1 \end{bmatrix}\begin {bmatrix} 1 & 2 & 1 \\ 0 & 2 & -2 \\ 0 & 4 & 1 \end{bmatrix}\\= \begin {bmatrix} 1 & 2 & 1 \\ 0 & 2 & -2 \\ 0 & 0 & 5 \end{bmatrix}$$

이처럼 matrix elimination을 matrix multiplication으로 표현할 수 있다.

## 결합 법칙

$$E_{32}(E_{21}A) = u$$
$$(E_{32}E_{21})A = u$$

$$E_{32}E_{21} = \begin {bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & -2 & 1 \end{bmatrix}\begin {bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}\\= \begin {bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ 6 & -2 & 1 \end{bmatrix}$$

단, 교환법칙은 성립하지 않는다.

## Permutation Matrix
### col picture (오른쪽)

 $$\begin{bmatrix}a & b\\c & d\end{bmatrix}\begin{bmatrix}0 & 1\\1 & 0\end{bmatrix} = \begin{bmatrix}c & d\\a & b\end{bmatrix}$$




오른쪽 행렬의 첫 행 $\begin{bmatrix}0 & 1\end{bmatrix}$은 
$$ \begin{bmatrix}a \\ c\end{bmatrix}$$ 

에서 아무것도 가져오지 않고, 

$$\begin{bmatrix}b \\ d\end{bmatrix}$$

에서 하나를 가져온다. 라고 해석할 수 있다.

두 번째 행 $\begin{bmatrix}1 & 0\end{bmatrix}$은 $\begin{bmatrix}a & c\end{bmatrix}$에서 하나를 가져오고, $\begin{bmatrix}b & d\end{bmatrix}$에서 아무것도 가져오지 않는다. 라고 해석할 수 있다.

즉, 좌측 행렬의 열을 바꾸는 것이다.

### row picture(왼쪽)

$$\begin{bmatrix}0 & 1\\1 & 0\end{bmatrix} \begin{bmatrix}a & b\\c & d\end{bmatrix} = \begin{bmatrix}c & d\\a & b\end{bmatrix}$$


왼쪽 행렬의 첫 열 
$$\begin{bmatrix}0 \\ 1\end{bmatrix}$$
은 $\begin{bmatrix}a & b\end{bmatrix}$ 에서 아무것도 가져오지 않고, $\begin{bmatrix}c & d\end{bmatrix}$에서 하나를 가져온다. 라고 해석할 수 있다. 

두 번째 열 
$$ \begin{bmatrix}1 \\ 0\end{bmatrix} $$
은 $\begin{bmatrix}a & b\end{bmatrix}$에서 하나를 가져오고, $\begin{bmatrix}c & d\end{bmatrix}$에서 아무것도 가져오지 않는다. 라고 해석할 수 있다.

즉, 우측 행렬의 행을 바꾸는 것이다.

*해당 노트는 MIT의 Gilbert Strang 교수님의 Linear Algebra 강의를 바탕으로 작성되었습니다.