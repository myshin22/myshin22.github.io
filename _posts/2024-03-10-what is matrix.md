---
layout: single
title: "행렬이란 무엇인가?"
---
# row picture & column picture

간단한 두 개의 선형 방정식을 생각해보자.

$$2x -y = 0$$
$$-x +2y = 3$$

이를 matrix로 표현하면 다음과 같다.

$$\begin{bmatrix}
2 & -1 \\
-1 & 2
\end{bmatrix} \begin{bmatrix}
x \\
y
\end{bmatrix} = \begin{bmatrix}
0 \\
3
\end{bmatrix}$$

먼저, row picture로 바라보자 

$2x-y=0$ 과 $-x+2y=3$ 은 x=1, y=2 에서 만난다. 



다음으로 colunm picture로 바라보자.

$$x\begin{bmatrix}
2  \\
-1 
\end{bmatrix} +y\begin{bmatrix}
-1 \\
2
\end{bmatrix} = \begin{bmatrix}
0 \\
3
\end{bmatrix}$$

$\begin{bmatrix}
2  \\
-1 
\end{bmatrix}$ 과 $\begin{bmatrix} -1 \\ 2 \end{bmatrix}$, 두 column의 linear combination이다.

이는 아래의 그림과 같이 두 벡터의 linear combination으로 나타난다.

## 3 by 3 matrix에서의 예시

이제 3*3 matrix로 확장하여 생각해보자 

마찬가지로 3 개의 선형 방정식을 생각해보자.

$$2x -y = 0$$
$$-x +2y-z = -1$$
$$-3y+4z = 4$$

이를 matrix로 표현하면 다음과 같다.

$$\begin{bmatrix}
2 & -1 & 0 \\
-1 & 2 & -3 \\
0 & -1 & 4
\end{bmatrix} \begin{bmatrix}
x \\
y \\
z
\end{bmatrix} = \begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}$$

이때, 

$$A = \begin{bmatrix}
2 & -1 & 0 \\
-1 & 2 & -3 \\
0 & -1 & 4
\end{bmatrix}$$

$$X = \begin{bmatrix}
x\\
y\\
z
\end{bmatrix}$$

$$b = \begin{bmatrix}
0\\
-1\\
4\end{bmatrix}$$ 

로, $AX = b$ 로 표현할 수 있다.








row space에서 바라볼 때, 

$2x -y = 0$,$-x +2y-z = -1$,$-3y+4z = 4$ 3 개의 plane은 한 점에서 만난다. 

column space에서 바라볼 때,

$$x\begin{bmatrix}
2  \\
-1 \\
0
\end{bmatrix} +y\begin{bmatrix}
-1 \\
2 \\
-3
\end{bmatrix} +z\begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix} = \begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}$$

x = 0, y = 0, z = 1 일 때, 3개의 column의 linear combination으로 나타난다.


## 3D space

x,y,z 의 값을 각각 1,1,0으로 바꾼다면, 

$$1\begin{bmatrix}
2  \\
-1 \\
0
\end{bmatrix} +1\begin{bmatrix}
-1 \\
2 \\
-3
\end{bmatrix} +0\begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix} = \begin{bmatrix}
1 \\
1 \\
3
\end{bmatrix}$$

b의 값이 바뀐다.

그렇다면, 모든 b에 대해 $AX = b$ 를 만족하는 x가 존재하는가?

다르게 표현하면, columns의 linear combination으로 3D space를 채울 수 있는가?

주어진  $A = \begin{bmatrix}
2 & -1 & 0 \\
-1 & 2 & -3 \\
0 & -1 & 4
\end{bmatrix}$ 에서는 가능하다! 

왜냐하면, A가 invertible하기 때문이다. (즉, A의 column들이 linearly independent하기 때문이다.)
## 요약
$AX =b$ 를 row way와 column way로 바라볼 수 있다.  

$$\begin{bmatrix}
2 & 5 \\
1 & 3
\end{bmatrix} \begin{bmatrix}
1 \\
2
\end{bmatrix}$$

### row way(dot product) 

$$\begin{bmatrix}
2 \cdot 1 & 5 \cdot 2 \\
1 \cdot 1 & 3 \cdot 2
\end{bmatrix} = \begin{bmatrix}
12 \\
7
\end{bmatrix}$$

### column way

$$1\begin{bmatrix}
2  \\
1
\end{bmatrix} +2\begin{bmatrix}
5 \\
3
\end{bmatrix} = \begin{bmatrix}
12 \\
7
\end{bmatrix}$$

(이때, $Ax$ 는 $A$ columns의  linear combination으로 나타난다.)
