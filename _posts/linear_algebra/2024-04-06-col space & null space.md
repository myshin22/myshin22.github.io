---
layout: single
category: 선형대수
title: "col space & null space"
use_math: true
---

## requirements of vector space

1) v+w, cv는 space 안에 속해야 한다. 
2) 모든 cv+dw(linear combination) 는 space 안에 있어야 한다. 

## properties of vector space
<p align="center">
  <img src="https://myshin22.github.io/assets/images/24.04.06(1).png" width="300">
  <br> L : line through the origin  P : plane through the origin

</p>

both L and P are subspaces of $R^3$

### $P \cup L$ is not a subspace of $R^3$

왜냐하면 $V+W$가 성립하지 않는다. 

$L$ 에 있는 vector $V$ 와 $P$에 있는 vector $W$를 더하면 $L$과 $P$의 합집합인 평면 위에 있지 않다.

### $P \cap L$ is a subspace of $R^3$
$P \cap L$ 내의 vector인 $v$와 $w$ 는 항상 $L$과 $P$ 모두에 속하기 때문에 $v+w$도 $P \cap L$에 속한다. 

## Column Space of  A ; c(A)

$$A = \begin{bmatrix} 1 & 1 & 2 \\ 2 & 1 & 3 \\ 3 & 1 & 4 \\ 4 & 1 & 5\end{bmatrix}$$

- column space of A는 col A의 linear combination으로 이루어진다. 
- column space of A는 $R^4$의 subspace이다.
- column A는 $R^4$의 모든 dimension을 채우지 못한다.
- col A는 서로 independent하지 않다. 
  
- $co1 +col2 = col3 = \begin{bmatrix} 1 \\ 2 \\ 3 \\ 4 \end{bmatrix} + \begin{bmatrix} 1 \\ 1 \\ 1 \\ 1 \end{bmatrix}= \begin{bmatrix} 2 \\ 3 \\ 4 \\ 5 \end{bmatrix}$ 이므로 col3은 nothing new이다. 

- $R^4$ 의 2 Dimension만 채운다.



## Ax = b는 모든 b에 대하여 해가 존재하는가? 


$$Ax = \begin{bmatrix} 1 & 1 & 2 \\ 2 & 1 & 3 \\ 3 & 1 & 4 \\ 4 & 1 & 5\end{bmatrix}\begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = \begin{bmatrix} b_1 \\ b_2 \\ b_3 \\ b_4 \end{bmatrix} $$

아니다!!

$b$가 c(A)에 속할 때만 해가 존재한다. 

ex) $A\begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \\ 0 \end{bmatrix}$, $A\begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix} = \begin{bmatrix} 1 \\ 2 \\ 3 \\ 4 \end{bmatrix}$, $A\begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix} = \begin{bmatrix} 1 \\ 1 \\ 1 \\ 1 \end{bmatrix}$

## Null Space of  A ; N(A)

$$Ax = \begin{bmatrix} 1 & 1 & 2 \\ 2 & 1 & 3 \\ 3 & 1 & 4 \\ 4 & 1 & 5\end{bmatrix}\begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \\ 0 \end{bmatrix} $$

Null space of A는 $Ax=0$을 만족하는 모든 $x$의 집합이다.

가장 간단한 x로  $\begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$ 을 생각할 수 있다.

다음으로 $\begin{bmatrix} 1 \\ 1 \\ -1 \end{bmatrix}$ 을 생각할 수 있다. 이 벡터에 어떤 scalar를 곱해도 0이 된다. 

모든 $c\begin{bmatrix} 1 \\ 1 \\ -1 \end{bmatrix}$이 Ax=0을 만족한다. 

따라서, $N(A)$는 origin을 지나는 line, $R^3$의 subspace이다.

## Ax = 0 의 해는 항상 subspace인가?

1) if Av=0, Aw=0 이면 A(v+w)=0이다. 
   
   A(v+w) = Av + Aw = 0 + 0 = 0

2) if Av=0 이면 A(cv)=0이다. 

   A(cv) = c(Av) = c0 = 0