---
layout: single
category: 선형대수
tags: 
    행렬
    선형대수
    linear_algebra
    elimination
title: "Elimination Matrix"
use_math: true
---
# Elimination Matrix
일반적인 연립 일차 방정식의 풀입법을 생각해보자.

$$ \begin {cases}
\textcircled{1}\ x+2y+z = 2 \\
\textcircled{2}\ 3x +8y+z = 12\\
\textcircled{3}\ 4y+z = 2
\end{cases}$$

일반적으로 $x$를 제거하기 위하여 $\textcircled{1} *3 - \textcircled{2}$ 를 수행한다.

계수행렬 $A$만 생각해보자.

$$A = \begin{bmatrix}
1 & 2 & 1 \\
3 & 8 & 1 \\
0 & 4 & 1
\end{bmatrix}$$

연립방정식과 마찬가지로 $row2 - 3*row1$\
(2행 1열을 제거한다고 생각하자) 

이때, row1의 첫번째 원소인 1을 pivot이라고 한다.

$$\begin{bmatrix}
3 \\
8 \\
1
\end{bmatrix} - 3\begin{bmatrix} 1 \\ 2 \\ 1 \end{bmatrix} = \begin{bmatrix} 0 \\ 2 \\ -2 \end{bmatrix}$$

이제 2번째 행에 해당 값을 넣어주면 된다. 

$$\begin{bmatrix}
1 & 2 & 1 \\
0 & 2 & -2 \\
0 & 4 & 1
\end{bmatrix}$$

이제 3번째 행의 2번째 원소를 제거하기 위하여 $row3 - 2*row2$를 수행한다.

$$\begin{bmatrix}
1 & 2 & 1 \\
0 & 2 & -2 \\
0 & 0 & 5
\end{bmatrix}$$

주의할 것은 pivot은 0이 될 수 없다는 것이다.

# Augmented Matrix 

계수 행렬 A에 상수 행렬 b를 붙인 것을 Augmented Matrix라고 한다.

$$\begin{bmatrix}
1 & 2 & 1 & 2 \\
3 & 8 & 1 & 12 \\
0 & 4 & 1 & 2
\end{bmatrix}$$

이전과 마찬가지로 pivot을 설정하여 계산을 수행한다.

2행 1열을 제거하기 위하여 $row2 - 3*row1$을 수행한다.

$$\begin{bmatrix}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 4 & 1 & 2
\end{bmatrix}$$

이제 3행 2열을 제거하기 위하여 $row3 - 2*row2$를 수행한다.

$$\begin{bmatrix}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 0 & 5 & -10
\end{bmatrix}$$

결론적으로 3 개의 방정식이 나오는데 $5z = -10$이므로 $z = -2$, $2y - 2z = 6$이므로 $y = 1$, $x + 2y + z = 2$이므로 $x = 2$이다.

즉, $x = 0$, $y = 1$, $z = 2$이다.


*해당 노트는 MIT의 Gilbert Strang 교수님의 Linear Algebra 강의를 바탕으로 작성되었습니다.