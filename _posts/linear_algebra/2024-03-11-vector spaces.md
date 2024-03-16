---
layout: single
category: 선형대수
title: "Vector Spaces"
use_math: true
---

## Permutations
$P$ matrix 는 row를 exchange한다. 

$$A = LU $$
$$P A = LU$$

n*n matrix에 대하여 가능한 경우의 수는 $n!$ 이다.

## Symmetric Matrices
$A^T = A$ 이면, $A$는 $symmetric$이다.\
(ex)
$$\begin{bmatrix} 3 & 1 & 7 \\ 1 & 2 & 3 \\ 7 & 9 & 4 \end{bmatrix}$$

## $R^{T} R$
$R^T R$은 항상 $symmetric$이다.

(ex)

$$R^T R = \begin{bmatrix} 1 & 3 \\ 2 & 3 \\ 4 & 1 \end{bmatrix}\begin{bmatrix} 1 & 2 & 4 \\ 3 & 3 & 1\end{bmatrix} = \begin{bmatrix} 10 & 11 & 7 \\ 11 & 13 & 11 \\ 7 & 11 & 17 \end{bmatrix}$$

$$(R^T R)^T = R^T R^{TT}= R^TR$$

## Vector Spaces
$R^2$는 = 2D real vectors

$$\begin{bmatrix} 3 \\ 2 \end{bmatrix}, \begin{bmatrix} 0 \\ 0 \end{bmatrix}, \begin{bmatrix} \pi \\ e \end{bmatrix}$$

$R^3$ = 3 개의 실수 구성요소를 가진 모든 vectors \
$R^n$ = n 개의 실수 구성요소를 가진 모든 vectors

## Vector Space의 조건

vector space는 덧셈과 스칼라 곱에 대하여 닫혀 있어야 한다. \
= vector space 내의 모든 벡터들에 대하여 더하거나 스칼라 곱을 했을 때의 결과도 같은 공간 내의 벡터가 되어야 한다. \
= linear combination of vectors


## Not a Vector Space 

<p align="center">
  <img src="https://myshin22.github.io/assets/images/vector_space_1.png" width="300">
  <br> 그림1. 4분면 중 제 1사분면만 포함하는 경우
</p>

$$\begin{bmatrix} 3 \\ 2 \end{bmatrix} + \begin{bmatrix} 3 \\ 2 \end{bmatrix}, 3\begin{bmatrix} 3 \\ 2 \end{bmatrix}$$ 

더하거나 양수를 곱하는 건 가능하지만, 

$$-5\begin{bmatrix} 3 \\ 2 \end{bmatrix}$$

음수를 곱하면, 해당 범위에서 나가 제 3사분면으로 가게 된다. \
따라서 이 경우는 $vector\;space$가 아니다.

## Subspace
a vecoter space inside $R^2$에 대해 생각해보자. 

$$\begin{bmatrix} 3 \\ 2 \end{bmatrix} + \begin{bmatrix} 3 \\ 2 \end{bmatrix},3\begin{bmatrix} 3 \\ 2 \end{bmatrix},-5\begin{bmatrix} 3 \\ 2 \end{bmatrix}$$ 

모두 한 직선 위에 존재한다.\
즉, 덧셈과 스칼라 곱에 대하여 닫혀 있으므로, 이 직선은 $subspace$이다.

*모든 subspace는 원점을 포함해야 한다.

## Subspace of $R^2$
- $R^2$ 전체
-  $\begin{bmatrix} 0 \\ 0 \end{bmatrix}$ 을 통과하는 직선
-  zero vector, $\begin{bmatrix} 0 \\ 0 \end{bmatrix}$

## Subspace of $R^3$
- $R^3$ 전체
-  $\begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$ 을 통과하는 평면
-  $\begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$ 을 통과하는 직
-  zero vector, $\begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$

## Column Space

$$A = \begin{bmatrix} 1 & 3 \\ 2 & 3 \\ 4 & 1 \end{bmatrix}$$

A의 $column$은 $R^3$ 안에 존재한다. 

A의 $column$인 $\begin{bmatrix} 1 \\ 2  \\ 4  \end{bmatrix}$, $\begin{bmatrix} 3 \\ 3  \\ 1  \end{bmatrix}$ 에 대하여 

- 서로 더할 수 있어야 한다.
- 스칼라 곱을 할 수 있어야 한다.

즉, $A$의 $column$에 대하여 $linear\;combination$ 할 수 있어야 한다. 

가능한 모든 $linear\;combination$이 subspace를 형성한다. 이를 $column\;space$; $C(A)$라고 한다.

