# 날짜 : 2023-06-19 07:27

# 주제 : #Geometry #Complex #Kahler #Einstein #Bergman
---
# Abstract
본 강연에서는 푸앙카레 원반의 상수곡률 계랑을 일반차원 복소다양체 위의 켈러 계량으로 일반화하는 두 가지 방법으로써, 켈러-아인슈타인 계량과 버그만 계량을 소개한 뒤, 이 둘 사이의 연관 관계와 최신 연구동향에 대해 소개하고자 한다.
# 내용
>[!note]-  Kahler Geometry
Kahler Geometry = Complex Geometry $\cap$ Riemannian Geometry
Kahler Manifold = $X + J + g$ satisfying $\nabla J =0$ where $J$ is a tensor and $g$ is a Riemannian metric.

>[!question]- What is the canonical or best metric on a given complex mfd?
>1. Riemannian Geometry aspect : Kahler - Einstein Metric
>2. Complex Geometry aspect : Bergman Metric which is invariant under $\text{Aut}\left(X\right) = \left\{\varphi : X \to X : \text{holomorphic}\right\}$ 
## Poincare Metric
>[!example]- n=1
>$X$ : compact 1-dimensional complex manifold
>There is a uniformation theorem 
>$$d\tilde{X} = \frac{1}{\left(1+c\left(x^{2}+y^{2}\right)\right)^{2}}\left(dx \otimes dx + dy \otimes dy\right)$$
>denominator $\lambda$ then $K_{\hat{X}}=-\frac{\Delta\left(\log{\lambda}\right)}{2\lambda} = 4c$
>If $C=0$, $\lambda = \frac{\partial^{2}}{\partial z \partial \bar{z}}\left(\left|z\right|^{2}\right) = \frac{\partial^{2}}{\partial z \partial \bar{z}}\left(\frac{1}{C}\log{\left(1+C\left|z\right|^{2}\right)}\right)$
>Let the $\frac{1}{C}\log{\left(1+C\left|z\right|^{2}\right)}$ be a potential function
>

>[!question]- Higher Dimension?
>No uniformation theorem
>$$\Delta \varphi = e^{\varphi}$$
## Kahler - Einstein Metric
>[!note]- Riemannian metric $g$ is hemitian
>If $g\left(JX, JY\right) = g\left(X, Y\right)$
Remark of metric
>$g$ is hermitian $\leftrightarrow$ w\left(X,Y\right) \coloneq g \left(JX, Y\right)$

>[!note]- Hermintian metric $g$ is Kahler
>If $dw = 0$.
>Also denote $dz_{j}\coloneq dx_{j} + \sqrt{-1}dy_{j}$ and g_{jk}=g^{\mathbb{C}}\left(\frac{\partial}{\partial z_{j}}, \frac{\partial}{\partial \bar{z}_{k}}\right)\newline
>$g = \sum g_{ik} dz^{i}\otimes \overline{dz^{k}} \leftrightarrow \sqrt{-1}\sum_{j,k}g_{j,k}dz^{j} \vee \overline{dz^{k}}$

>[!note]- $g$ : Kahler- Einstein
>If $g$: Kahler, $\text{Ric}_{g}\left(X, X\right) = \frac{\text{Ric}_{g}\left(X,X\right)}{g\left(X, X\right)} = C$

[Complex Monge - Ampere Equation](https://en.wikipedia.org/wiki/Monge%E2%80%93Amp%C3%A8re_equation) #Non-linear #PDE

## Bergman metric
Kobayashi
Bergman kernel form

# Conclusion
1. Berman metric $B_{X}, w_{X}$ : invariant under $\text{Aut}\left(X\right)$
2. $X$ : bounded homogeneous domain $\subset \mathbb{C}^{n}$
3. $X$: cpt $\Rightarrow \int_{X} B_{X} = \text{dim}_{\mathbb{C}}\Omega_{2}^{n,0}\left(X\right)= \text{dim}_{\mathbb{C}}\mathcal{H}_{2}^{n,0}\left(X\right)$
# 출처(참고문헌)
-

## 연결문서
[[Complex Geometry]]
[[Geometry SOP]]
[[Einstein Manifold]]
[[Kahler Manifold]]
[[Complex Monge - Ampare Equation]]