---
layout: single
category: 선형대수
title: "Matrix Multiplication in 4 Ways"
use_math: true
---
## First Way. (row of A) * (col of B)

$$ AB = C$$

$$\begin {bmatrix} a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33} \end{bmatrix} \begin {bmatrix} b_{11}&b_{12}&b_{13}\\b_{21}&b_{22}&b_{23}\\b_{31}&b_{32}&b_{33} \end{bmatrix} = \begin {bmatrix}c_{11}&c_{12}&c_{13}\\c_{21}&c_{22}&c_{23}\\c_{31}&c_{32}&c_{33} \end{bmatrix}$$

$$c_{21}  = (row2\ of\ A)(col1\ of\ B) \\ = a_{21}b_{11} + a_{22}b_{21} + a_{23}b_{31}\\ = \sum_{k=1}^{3} a_{2k}b_{k1}$$


## Second Way. Colunm Picture

$$ AB = C$$

$$\begin {bmatrix} a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33} \end{bmatrix} \begin {bmatrix} b_{11}&b_{12}&b_{13}\\b_{21}&b_{22}&b_{23}\\b_{31}&b_{32}&b_{33} \end{bmatrix} = \begin {bmatrix}c_{11}&c_{12}&c_{13}\\c_{21}&c_{22}&c_{23}\\c_{31}&c_{32}&c_{33} \end{bmatrix}$$

$A$의 column은 각각

$$
\begin{bmatrix}
a_{11} \\
a_{21} \\
a_{31}
\end{bmatrix},
\begin{bmatrix}
a_{12} \\
a_{22} \\
a_{32}
\end{bmatrix},
\begin{bmatrix}
a_{13} \\
a_{23} \\
a_{33}
\end{bmatrix}
$$

column picture는 오른쪽에서부터 multiplication을 한다.

$$
C의 \; col1 = 
\begin{bmatrix}
c_{11} \\
c_{21} \\
c_{31}
\end{bmatrix} 
= 
b_{11} 
\begin{bmatrix}
a_{11} \\
a_{21} \\
a_{31}
\end{bmatrix} 
+ 
b_{12} 
\begin{bmatrix}
a_{12} \\
a_{22} \\
a_{32}
\end{bmatrix} 
+ 
b_{13} 
\begin{bmatrix}
a_{13} \\
a_{23} \\
a_{33}
\end{bmatrix}
$$


즉, $C$의 각 column은 $A$의 각 column의 linear combination이다.


## Third Way. Row Picture

$$ AB = C$$

$$\begin {bmatrix} a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33} \end{bmatrix} \begin {bmatrix} b_{11}&b_{12}&b_{13}\\b_{21}&b_{22}&b_{23}\\b_{31}&b_{32}&b_{33} \end{bmatrix} = \begin {bmatrix}c_{11}&c_{12}&c_{13}\\c_{21}&c_{22}&c_{23}\\c_{31}&c_{32}&c_{33} \end{bmatrix}$$

$B$의 row는 각각 $row1= \begin {bmatrix}b_{11}&b_{12}&b_{13}\end{bmatrix}$, $row2= \begin {bmatrix}b_{21}&b_{22}&b_{23}\end{bmatrix}$, $row3= \begin {bmatrix}b_{31}&b_{32}&b_{33}\end{bmatrix}$ 이다.

row picture는 왼쪽에서부터 multiplication을 한다.

즉, $C$의 $row1 = \begin{bmatrix}c_{11}&c_{12}&c_{13}\end{bmatrix} = \begin{bmatrix}b_{11}&b_{12}&b_{13}\end{bmatrix}a_{11} + \begin{bmatrix}b_{21}&b_{22}&b_{23}\end{bmatrix}a_{12} + \begin{bmatrix}b_{31}&b_{32}&b_{33}\end{bmatrix}a_{13}$ 이다.

## Fourth Way. Sum of (col of A) * (row of B)

$$ AB = C$$

$$\begin {bmatrix} a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33} \end{bmatrix} \begin {bmatrix} b_{11}&b_{12}&b_{13}\\b_{21}&b_{22}&b_{23}\\b_{31}&b_{32}&b_{33} \end{bmatrix} \\= \begin {bmatrix} a_{11}\\a_{21}\\a_{31}\end{bmatrix} \begin {bmatrix} b_{11}&b_{12}&b_{13} \end{bmatrix} + \begin {bmatrix} a_{12}\\a_{22}\\a_{32}\end{bmatrix} \begin {bmatrix} b_{21}&b_{22}&b_{23} \end{bmatrix} + \begin {bmatrix} a_{13}\\a_{23}\\a_{33}\end{bmatrix} \begin {bmatrix} b_{31}&b_{32}&b_{33} \end{bmatrix}$$

예를 들어 설명하자면, 

$$\begin {bmatrix} 2& 7 \\ 3 & 8 \\ 4 & 9 \end{bmatrix}\begin {bmatrix} 1 & 6 \\ 0 & 0 \end{bmatrix}\\= \begin {bmatrix} 2\\3\\4\end{bmatrix} \begin {bmatrix} 1 & 6 \end{bmatrix} + \begin {bmatrix} 7\\8\\9\end{bmatrix} \begin {bmatrix} 0 & 0 \end{bmatrix} \\= \begin {bmatrix} 2 & 12 \\ 3 & 18 \\ 4 & 24 \end{bmatrix} + \begin {bmatrix} 0 & 0 \\ 0 & 0 \\ 0 & 0 \end{bmatrix} \\= \begin {bmatrix} 2 & 12 \\ 3 & 18 \\ 4 & 24 \end{bmatrix}$$


## Block 

$$AB \\= \begin {bmatrix} A_{1}&A_{2}\\A_{3}&A_{4} \end{bmatrix}\begin {bmatrix} B_{1}&B_{2}\\B_{3}&B_{4} \end{bmatrix}\\= \begin{bmatrix} C_{1}&C_{2}\\C_{3}&C_{4} \end{bmatrix}$$

$$C_{1} = A_{1}B_{1} + A_{2}B_{3}$$



