---
layout: single
category: 통계적 추론
title: "Convergence in probability"
use_math: true
---
## Convergence in probability 
$$lim_{n \to \infty} P(|X_n - X| > \epsilon) = 0$$

$$ X_n \overset{p}{\to} X \ as \ n \to \infin$$

## Basic tools to show $\overset{p}{\to}$
### (1) Markov's Inequality 

>$u(X) \geq 0$이 $r.v.X$의 함수이고,$E\{u(x)\}$이 존재할 때 any constant $c > 0$에 대하여 다음이 성립한다.
>$$P(u(X) \geq c) \leq \frac{E\{u(X)\}}{c}$$

1) $u(X_n - X) = (X_n - X)^2$ 
2) $E(X_n-X)^2 \overset{p}{\to} 0$ for any $c =\epsilon >0$ \
일 때, $X_n \overset{p}{\to} X$ 를 보일 수 있다.   

샌드위치 theorem으로, 
$$ P( (X_n - X)^2 \geq c) \leq \frac{E(X_n - X)^2}{c} \to 0$$ 
에서 $P( (X_n - X)^2 \geq c) \to 0$ 가 된다. 
### (2) Weak law of large numbers (WLLN)
>$\{X_n\}$이 common mean $\mu\in R$과 variance $\sigma^2<\infin$을 갖는 iid r.v. 이고,  $\bar{X_n} = n^{-1}\sum_{i=1}^{n}X_i$ 일 때,
>$$\bar{X_n} \overset{p}{\to} \mu$$

(proof) $E(\bar{X_n}) = \mu, Var(\bar{X_n}) = \frac{\sigma^2}{n}$ 이고, $\epsilon > 0$ 일 때, 체비셰프 부등식에 의하여 

$$P(|\bar{X_n} - \mu| \geq \epsilon) \leq \frac{\sigma^2}{n\epsilon^2} \to 0 \\(\because \sigma, \epsilon \ \  constant )$$

(remark) 만약 $X_n$ 이 sample mean이고, ${X_n} \overset{p}{\to} X$를 보이고 싶다면, WLLN을 이용할 수 있다. 

cf) chebyshev's inequality
$$P(|X - \mu| \geq \epsilon) \leq \frac{\sigma^2}{\epsilon^2}$$
(proof) $E(X) = \mu, Var(X) = \sigma^2$ 일 때, $E(X^2) = \int_{-\infty}^{\infty}x^2f(x)dx$ 이고, $E(X^2) \geq \int_{|X - \mu| \geq \epsilon}x^2f(x)dx \geq \epsilon^2P(|X - \mu| \geq \epsilon)$

## proof of markov's inequality & chebyshev's inequality
### markov's inequality
>$$ P(x \geq \alpha) \leq \frac{E(x)}{\alpha}$$

$$E(x) = \int_{0}^{\infty} x f(x) dx \\=\int_{0}^{\alpha}xf(x)dx+ \int_{\alpha}^{\infin}xf(x)dx \geq \int_{\alpha}^{\infin}xf(x)dx (\because \alpha \geq 0)$$
$$\int_{\alpha}^{\infin}xf(x)dx \geq \int_{\alpha}^{\infin}\alpha f(x)dx$$ 
$$E(x) \geq \alpha \int_{\alpha}^{\infin}f(x)dx = \alpha P(x \geq \alpha)$$

$$\therefore P(x \geq \alpha) \leq \frac{E(x)}{\alpha}$$

### chebyshev's inequality
>임의의 r.v. $X$와 $\alpha > 0$에 대하여 다음이 성립한다.
>$$P(|X - \mu| \geq \alpha) \leq \frac{var(X)}{\alpha^2}$$

$$|X - E(x)| \geq \alpha \Leftrightarrow (X - E(x))^2 \geq \alpha^2$$
새로운 r.v. $Y$를 정의하면,
$$ Y = (X - E(x))^2$$
분산의 정의에 의해, $E(Y) = Var(X)$ 이다.

$Y와 \alpha^2$에 대한 마르코프 부등식에 의하여,
$$P(Y \geq \alpha^2) \leq \frac{E(Y)}{\alpha^2}$$
이를 다시 X에 대한 식으로 나타내면,
$$P((X - E(X))^2 \geq \alpha^2) \leq \frac{Var(X)}{\alpha^2}$$
$$\therefore P(|X - \mu| \geq \alpha) \leq \frac{Var(X)}{\alpha^2}$$