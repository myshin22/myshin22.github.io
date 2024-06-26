---
layout: single
category: 통계적 추론
title: "Convergence in probability"
use_math: true
---
## Convergence in probability 

$$ X_n \overset{p}{\to} X $$

${X_n}$이 r.v. sequence이고, $X$가 sample space에서 정의된 r.v.일 때, 모든 $\epsilon > 0$에 대하여  $X_n$ convergences in probability to X

>$$lim_{n \to \infty} P(|X_n - X| > \epsilon) = 0 $$

## Basic tools to show $\overset{p}{\to}$
### (1) Markov's Inequality 

$u(X) \geq 0$이 $r.v.X$의 함수이고,$E(u(x))$이 존재할 때 any constant $c > 0$에 대하여 다음이 성립한다.

>$$P(u(X) \geq c) \leq \frac{E(u(X))}{c}$$

1) $u(X_n - X) = (X_n - X)^2$ \
2) $E(X_n-X)^2 \overset{p}{\to} 0$ for any $c =\epsilon >0$ \
일 때, $X_n \overset{p}{\to} X$ 를 보일 수 있다.   

샌드위치 theorem으로, 

$$ P( (X_n - X)^2 \geq c) \leq \frac{E(X_n - X)^2}{c} \to 0$$ 
에서 $P( (X_n - X)^2 \geq c) \to 0$ 가 된다. 

### (2) Weak law of large numbers (WLLN)
임의의 확률변수의 표본 평균이 그 확률변수의 기댓값(모평균)에 확률적으로 수렴한다. 

$\{X_n\}$이 common mean $\mu\in R$과 variance $\sigma^2<\infty$을 갖는 iid r.v. 이고,  $\bar{X_n} = n^{-1}\sum_{i=1}^{n}X_i$ 일 때,

>$$\bar{X_n} \overset{p}{\to} \mu$$

(proof) $E(\bar{X_n}) = \mu, Var(\bar{X_n}) = \frac{\sigma^2}{n}$ 이고, $\epsilon > 0$ 일 때, 체비셰프 부등식에 의하여

$$cf)\  P(|X - \mu| \geq \alpha) \leq \frac{var(X)}{\alpha^2} $$

$$P(|\bar{X_n} - \mu| \geq \epsilon) \leq \frac{\sigma^2}{n\epsilon^2} \to 0 \\(\because \sigma, \epsilon \ \  constant )$$

(remark) 만약 $X_n$ 이 sample mean이고, ${X_n} \overset{p}{\to} X$를 보이고 싶다면, WLLN을 이용할 수 있다. 



## proof of markov's inequality & chebyshev's inequality
### markov's inequality
$$ P(x \geq \alpha) \leq \frac{E(x)}{\alpha}$$
X에 대한 기댓값은 다음과 같다. 

>$$ E(x) = \int_{0}^{\infty} x f(x) dx $$

이를 $\alpha$를 기준으로 나눠 쓸 수 있다. 

$$ =\int_{0}^{\alpha}xf(x)dx+ \int_{\alpha}^{\infty}xf(x)dx \geq \int_{\alpha}^{\infty}xf(x)dx (\because \alpha \geq 0) $$

$\alpha f(\alpha)+(\alpha +1)f(\alpha +1)+.. \geq \alpha f(\alpha)+\alpha(\alpha +1)+..$ 이므로 다음이 성립한다. 

$$ \int_{\alpha}^{\infty}xf(x)dx \geq \int_{\alpha}^{\infty}\alpha f(x)dx $$ 

식을 정리하면, 

$$ E(x) \geq \alpha \int_{\alpha}^{\infty}f(x)dx = \alpha P(x \geq \alpha) $$

$$\therefore P(x \geq \alpha) \leq \frac{E(x)}{\alpha}$$

### chebyshev's inequality
임의의 r.v. $X$와 $\alpha > 0$에 대하여 다음이 성립한다.

>$$ P(|X - \mu| \geq \alpha) \leq \frac{var(X)}{\alpha^2} $$

$$ |X - E(x)| \geq \alpha \Leftrightarrow (X - E(x))^2 \geq \alpha^2 $$

새로운 r.v. $Y$를 정의하면,

$$ Y = (X - E(x))^2 $$

분산의 정의에 의해, $E(Y) = Var(X)$ 이다.

$Y와 \alpha^2$에 대한 마르코프 부등식에 의하여,

$$ P(Y \geq \alpha^2) \leq \frac{E(Y)}{\alpha^2} $$

이를 다시 X에 대한 식으로 나타내면,

$$ P((X - E(X))^2 \geq \alpha^2) \leq \frac{Var(X)}{\alpha^2} $$

$$ \therefore P(|X - \mu| \geq \alpha) \leq \frac{Var(X)}{\alpha^2} $$

*해당 노트는 Hogg, R. V., McKean, J. W., & Craig, A. T. (2020). Introduction to mathematical statistics (8th ed.). Upper Saddle River, N.J: Pearson Prentice Hall.와 성균관대학교 이경재 교수님의 통계적 추론 입문 강의를 바탕으로 작성되었습니다. *