---
permalink: /projects/DCPonProj/ProjLinGrpDim1/Dihedral
title: "Dimension1 Dihedral"
author_profile: true
---


When $n$ is odd, group $G=D_n$ with representation given by

$$
\begin{align*}
G=\langle
\begin{pmatrix}
\zeta_n^s & 0 \\
0 & \zeta_n^{-s}
\end{pmatrix},
\begin{pmatrix}
0 & 1\\
1 & 0
\end{pmatrix}
\rangle,
\end{align*}
$$

where $\zeta_n$ is a $n$-th root of unity, $s$ is coprime to $n$.

When $n$ is even, group $G=D_n$ with projective representation given by

$$
\begin{align*}
G=\langle
\begin{pmatrix}
\zeta_{2n}^s & 0 \\
0 & \zeta_{2n}^{-s}
\end{pmatrix},
\begin{pmatrix}
0 & 1\\
1 & 0
\end{pmatrix}
\rangle,
\end{align*}
$$


where $\zeta_{2n}$ is a $2n$-th root of unity, $s$ is coprime to $2n$.


Here we take $n=3$ as an example, the magma code is as follows:
<pre>

n:=3;

FScale:=CyclotomicField(n:Sparse:=true);

F:=FScale;

Zn:=F.1;

s:=1;

G:=MatrixGroup<2,F|
[Zn^s,0, 0,Zn^(-s)],
[0,1, 1,0]>;

</pre>

For general $n$ and $s$ coprime to $n$, the Burnside symbol is
$$
\begin{align*}
[\mathbb{P}^1 \circlearrowleft G]=&(1,C_n \circlearrowright k(x),())\\
&+(C_n,1 \circlearrowright k,(s))+(C_n,1 \circlearrowright k,(n-s))
\end{align*}
$$