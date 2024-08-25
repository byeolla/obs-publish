---
tags:
  - Low-dimensional
  - 3d
  - Knot
  - essential
  - Boundary
  - boundary_parallel
  - compressing
  - compressible
  - incompressible
aliases:
  - boundary incompressible surface
  - essential surface
  - inessential surface
  - incompressible surface
---
[[Low Dimensional Topology]]

Let $S$ be a compact surface ***properly embedded*** in a smooth 3 - [[Manifold|manifold]] $M$.
# Compressible Disk
A `compressing disk` $D$ is a disk embedded in $M$ such that $D \cap S = \partial D$ and the intersection is transverse.

If the curve $\partial D$ does not bound a disk inside of $S$, then $D$ is called a ***nontrivial*** compressing disk.

If $S$ has a nontrivial compressing disk, then we call $S$ a ***compressible*** surface in $M$.

If $S$ is neither the $S^{2}$ nor a ***compressible*** surface, then we call the surface ***incompressible***. 

>[Example in stack](https://math.stackexchange.com/questions/4489293/how-to-visualize-a-compressible-surface-in-3-manifold-m)


![[Incompressible disck.png]]

$D$ is a compressible disk.
# $\partial$-incompressible
A properly embedded surface $S\subset M$ is $\partial$-incompressible if for each disk $D \subset M$ such that $\partial D \cap S$ is an arc $\alpha$ in $\partial D$ and $\partial D \setminus \alpha \subset \partial M$ (such a $D$ is called a $\partial$ - ***compressing*** disk for $S$) there is a disk $D^{\prime} \subset S$ with $\alpha \subset \partial D^{\prime}$ and $\partial D^{\prime} \setminus \alpha \subset \partial M$.
![[bdry-compressible.png]]
boundary compressible disk

# Essential Surface
A surface which is either incompressible and $\partial$ - incompressible, or a sphere not bounding a ball, or a disk that is not [[boundary parallel]], will be called an `essential` surface.


Given a [[Chapter 1(Smooth Manifolds)#Definition. Closed & Open Manifold|closed surface]] $F$ in $S^{3}$ containing a link $L$, we say that $F$ is ***essential*** with respect to $L$ when $F \cap \left(S^{3}\setminus \nu\left(L\right)\right)$ is essential in $S^{3}\setminus \nu\left(L\right)$. When $L$ is clear, we may simply write that $F$ is essential.


