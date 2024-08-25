---
tags:
  - Mathematics
---
```toc
```
# Topological Manifolds
---
# Smooth Structure
---
# Examples of Smooth Manifolds
---
# Manifolds with Boundary
### Definition
**Definition.** Closed n-dimensional upper half-space 
Define $\mathbb{H}^{n}$ as $\mathbb{H}^{n} = \left\{\left(x^{1}, \dots, x^{n}\right) \in \mathbb{R}^{n} : x^{n} \geq 0 \right\}$.
Then ***closed n-dimensional upper half-space*** $\mathbb{H}^{n} \subseteq \mathbb{R}^{n}$
$\text{Int}\mathbb{H}^{n} = \left\{\left(x^{1}, \dots, x^{n}\right) \in \mathbb{R}^{n} : x^{n} > 0 \right\}$.
$\partial\mathbb{H}^{n} =  \left\{\left(x^{1}, \dots, x^{n}\right) \in \mathbb{R}^{n} : x^{n} = 0 \right\}$.

We just need to define a ***chart $\left(U, \varphi \right)$ for $\mathbf{M}$*** 
***Interior chart***  if $\varphi \left(U\right)$ is an open subset of $\mathbb{R}^{n}$
***Boundary Chart*** if $\varphi \left( U \right)$ is an open subset of $\mathbb{H}^{n}$ such that $\varphi \left( U \right) \cap \partial \mathbb{H}^{n} \neq \emptyset$
### Theorem 1.37. Topological Invariance of the Boundary
If $\mathbf{M}$ is a topological manifold with boundary, then each point of $\mathbf{M}$ is either a boundary point or an interior point, but not both. Thus $\partial \mathbf{M}$ and $\text{Int}\mathbf{M}$ are disjoint sets whose union is $M$.

#### *Differences about boundary in topological of manifold*
In the point of view the closed unit ball $\bar{\mathbb{B}}^{n}$, is a manifold with bounday, whose manifold boundary is $\mathbb{S}^{n-1}$ as well as view it as a subset of $\mathbb{R}^{n}$ then topological boundary is $\mathbb{S}^{n-1}$.

However, if we think of $\bar{\mathbb{B}}^{n}$ as a topological space in its own right, then as a subset of itself, it has empty topological boundary. Also, if we think of it as a subset of $\mathbb{R}^{n+1}$, its topological boundary is all of $\bar{\mathbb{B}}^{n}$ is all of itself.

Note that $\mathbb{H}^{n}$ is tiself a manifold with boundary, and its manifold is the same as its topological boundary as a subset of $\mathbb{R}^{n}$.

Every interval in $\mathbb{R}$ is a 1-manifold with boundary, whose manifold boundary consists of its endpoints.

### Definition. Closed & Open Manifold
- ***Closed Manifold***
	>A compact manifold without boundary
- ***Open Manifold***
	>A noncompact manifold without boundary

### Proposition 1.38
Let $\mathbf{M}$ be a topological $n$-manifold with boundary
1. $\text{Int}\mathbf{M}$ is an open subset of $\mathbf{M}$ and a topological $n$-manifold without boundary.
2. $\partial\mathbf{M}$ is a closed subset of $\mathbf{M}$ and a topological $\left(n-1\right)$-manifold without boundary.
3. $\mathbf{M}$ is a topological manifold $\iff$ $\partial\mathbf{M} = \emptyset$
4. If $n=0$, then $\partial \mathbf{M}=\emptyset$ and $\mathbf{M}$ is a $0$-manifold.

## Smooth Structures on Manifolds with Boundary
