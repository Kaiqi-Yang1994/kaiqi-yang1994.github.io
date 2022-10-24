---
permalink: /projects/CompBnG/examples
title: "Projects"
author_profile: true
---

Take symmetric group $G=\mathcal{S}_5$ as an example.

Compute $\mathcal{BC}_n(G)$ by definition:


<ul>
<li>Open the magma code that computes group $\mathcal{BC}_n(G)$ by definition.
<li>Copy all lines of code and paste in Magma.
<li>Let $G=\mathcal{S}_5.n=2$ and compute $\mathcal{BC}_n(G)$:
```
G:=SymmetricGroup(5);
BC,FullLattice,QuoMap,Generators,IndSet2,RelationBase:=BrutalBC(G,2);
```
![My Image](http://kaiqi-yang1994.github.io/files/bcn/BnGexamplestep1.png)
</ul>
