---
layout: single
category: 회귀분석
title: "Mean Squared Error"
use_math: true
---
## 용어 정리 

### Mean Squared Error (MSE)
$MSE$는 $E[(추정치 - 실제값)^2]$이다. 

$$MSE = E[(\hat{\theta} - \theta)^2]$$

### Bias
$Bias$는 $E[추정치 - 실제값]$이다.

$$Bias = E[\hat{\theta} - \theta]$$

### Variance
$Variance$는 $E[(추정치 - 기댓값)^2]$이다.

$$Var = E[(\hat{\theta} - E[\hat{\theta}])^2]$$

## MSE의 성질
$$ MSE =  Var + Bias^2 $$

우선 MSE의 정의는 다음과 같다. 

$$ E[(\hat{\theta} - \theta)^2] $$

해당 식 안에 $E(\hat\theta)$를 빼고 더한다. 

$$ E[(\hat{\theta} - E[\hat{\theta}] + E[\hat{\theta}] - \theta)^2] $$

이를 전개하면, 

$$ E[(\hat{\theta} - E[\hat{\theta}])^2 + 2(\hat{\theta} - E[\hat{\theta}])(E[\hat{\theta}] - \theta) + (E[\hat{\theta}] - \theta)^2] $$

이때, $E[\hat{\theta}] - \theta$는 상수이다. \
recall that E(ax) = aE(x), E(a) = a

$$ E[(\hat{\theta} - E[\hat{\theta}])^2] + 2(E[\hat{\theta}] - \theta)E[(\hat{\theta} - E[\hat{\theta}])] + (E[\hat{\theta}] - \theta)^2 $$

$E[(\hat{\theta} - E[\hat{\theta}])]$ = 0 이므로,

$$ E[(\hat{\theta} - E[\hat{\theta}])^2] + (E[\hat{\theta}] - \theta)^2 $$

이를 정리하면, 

$$ MSE =  Var + Bias^2 $$
