---
tags:
  - Mathematics/Smooth
  - Mathematics/POU
---
```toc
```

```
Notation
1. Function
> codomain is that a ***real-valued function***
2. Map or Mapping
>Any type of map, such as a map between arbitrary manifolds.
```

# Smooth Functions and Smooth Maps
---
---
## Smooth Functions on Manifolds
---

### Smooth Function
**Definition.** Smooth function
$\mathbf{M}$ is a smooth $n$-manifold, $k \in \mathbf{Z}_{\ge0}$ , and $f: \mathbf{M} \to \mathbb{R}^{k}$ is any function. Then $f$ is a ***smooth function***
if $\forall p \in \mathbf{M}$, there exists a smooth chart $\left(U, \phi\right)$ for $\mathbf{M}$ whose domain contains $p$ and such that the composite function $f \circ \phi^{-1}$ is a smooth on the open subset $\hat{U} = \phi \left(U \right) \subseteq \mathbb{R}^{n}$. 

If $\mathbf{M}$ is a smooth manifold with boundary, $\phi(U)$ is now an open subset of either $\mathbb{R}^{n}$ or $\mathbb{H}^{n}$

#### Remarkd and Exercise 2.1 [Linear Algebra](Bilinear.md) #Mathematics/Algebra
$C^{\infty}\left(\mathbf{M}\right) = \left\{f: \mathbf{M} \to \mathbf{R} \text{which is smooth real-valued functions}\right\}$
**Property**
1. $C^{\infty}\left(\mathbf{M}\right)$ is a vector space over $\mathbb{R}$.
2. [[Commutative Ring]]
3. A commutative and associative algebra over R [[Bilinear#Algebra over $ mathbb{R}$|bilinear]].



#### Exercise 2.2
$U$ be an open submanifold of $\mathbb{R}^{n}$ with its standard smooth manifold structure.
$f: U \to \mathbb{R}^{k}$ is smooth in the sense just defined $\iff$ it is a smooth in the sense of ordinary calculus.
Also for open submanifold with boundary in $\mathbb{H}^{n}$ 

#### Exercise 2.3
$\mathbf{M}$ : smooth manifold with or without boundary, and $f : \mathbf{M} \to \mathbb{R}^{k}$ is a smooth function. Then $f \circ \phi^{-1} : \phi\left(U\right) \to \mathbb{R}^{k}$ is smooth for *every* smooth chart $\left(U, \phi \right)$ for $\mathbf{M}$. 

***Proof.*** Since $f$ is a smooth function,  $\exists$ smooth chart $\left(V, \psi\right)$ that chart domain and $f \circ \psi^{-1}$ is a smooth function. Also, $\mathbb{M}$ is a smooth manifold that $\psi \circ \phi^{-1}$ is smooth function. Therefore, $f \circ \psi^{-1} \circ \psi \circ \phi^{-1} = f \circ \phi^{-1}$ is a smooth for every smooth chart $\left(U, \phi \right)$ for $\mathbb{M}$. 

### Coordinate representation of $f$
**Definition.** Coordinate Representation of $f$ 
Given a function $f : \mathbf{M} \to \mathbf{R}^{k}$ and a chart $\left(U, \phi \right)$ for $\mathbf{M}$, the function $\hat{f} : \phi\left(U \right) \to \mathbb{R}^{k}$ defined by $\hat{f} (x) = f \circ \phi^{-1}(x)$ is called the ***coordinate representation of $f$***. 

**Property.**
1. $f$ is smooth $\iff$ its coordinate representation is smooth in some smooth chart around each point. By definition
2. Smooth functions have smooth coordinate representations in every smooth chart.


<font color='red'>Meaning</font>
In keeping with our practice of using local coordinates to identify an open subset of a manifold with an open subset of Euclidean space, in cases where it causes no confusion we often do not even observe the distinction between $\hat{f}$ and $f$ itself. 
결국 표현할 수 있는 하나만 구하면 된다는 이야기임

---
## Smooth Maps Between Manifolds


---


# Partitions of Unity
---
---
