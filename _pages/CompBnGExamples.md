---
permalink: /projects/CompBnG/examples
title: "Projects"
author_profile: true
---

Take symmetric group $G=\mathcal{S}_5$ as an example.

Compute $\mathcal{BC}_n(G)$ by definition:


<ul>
<li>Open the magma code that computes group $\mathcal{BC}_n(G)$ by definition, copy all lines of code and paste in Magma.</li>
<li>Let $G=\mathcal{S}_5, n=2$ and compute $\mathcal{BC}_n(G)$:
  
```
G:=SymmetricGroup(5);
BC,FullLattice,QuoMap,Generators,IndSet2,RelationBase:=BrutalBC(G,2);
```
![My Image](http://kaiqi-yang1994.github.io/files/bcn/BnGexamplestep1.png)</li>
<li> The result is $\mathcal{BC}_2(G)=(\mathbb{Z}/2)^6 \times \mathbb{Z}/4$.
![My Image](http://kaiqi-yang1994.github.io/files/bcn/BnGexamplestep2.png)</li>
<li>Open the magma code that computes group $\mathcal{BC}_n(G)$ by decomposition, copy all lines of code and paste in Magma.</li>
<li>Compute $\mathcal{BC}_n(G)$:
![My Image](http://kaiqi-yang1994.github.io/files/bcn/BnGexamplestep3.png)</li>
<li>Type the following code:
~~~
for i in [1..#Out] do
	if Type(Out[i][1]) eq RngIntElt then
		i,0;
	else
		i,Moduli(Out[i][1]);
	end if;
end for;

S:=[];
for i in [1..#Out] do
	if Type(Out[i][1]) eq RngIntElt then
	else
		S:=S cat Moduli(Out[i][1]);
	end if;
end for;
SequenceToMultiset(S);
~~~
We see result:
![My Image](http://kaiqi-yang1994.github.io/files/bcn/BnGexamplestep4.jpg)</li>
</ul>
