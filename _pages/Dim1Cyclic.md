---
permalink: /projects/DCPonProj/ProjLinGrpDim1/Cyclic
title: "Dimension1 Cyclic"
author_profile: true
---

The group $G=C_n$ has a representation given by

$$
\begin{align*}
G=\langle
\begin{pmatrix}
1 & 0 \\
0 & \zeta_n^s
\end{pmatrix}
\rangle,
\end{align*}
$$

where $\zeta_n$ is a nth root of unity, $s$ is coprime to $n$.

Here we take $n=3$ as an example, the magma code is as follows:
<pre>

n:=3;

FScale:=CyclotomicField(n:Sparse:=true);

F:=FScale;

Zn:=F.1;

s:=1;

G:=MatrixGroup<2,F|
[1,0, 0,Zn^s]>;

</pre>

For general $n$ and $s$ coprime to $n$, the Burnside symbol is
$$
\begin{align*}
[\mathbb{P}^1 \circlearrowleft G]=&(1,G \circlearrowright k(x),())\\
&+(C_n,1 \circlearrowright k,(s))+(C_n,1 \circlearrowright k,(n-s))
\end{align*}
$$