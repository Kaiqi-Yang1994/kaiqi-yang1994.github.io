---
permalink: /projects/DCPonProj/C3extRank2
title: "Example C_n^2:C_3"
author_profile: true
---

Group $G=C_n^2:C_3$ is described by the short exact sequence

$$
\begin{align*}
1 \to C_n \oplus C_n \to G \to C_3 \to 1
\end{align*}
$$

When $n=5$, group $G=C_5^2:C_3 \subseteq \rm{PGL}(3,\mathbb{C})$, it has 2 projective linear representations $\mathbb{P}(V_1),\mathbb{P}(V_2)$ where

$$
\begin{align*}
G=
\langle
g_{n,s}^1=\begin{pmatrix}
\zeta_n^s & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{pmatrix},
g_{n,t}^2=\begin{pmatrix}
1 & 0 & 0\\
0 & \zeta_n^t & 0\\
0 & 0 & 1
\end{pmatrix},
\begin{pmatrix}
0 & 0 & 1\\
1 & 0 & 0\\
0 & 1 & 0
\end{pmatrix}
\rangle \subseteq \rm{PGL}(3,\mathbb{C}).
\end{align*}
$$

where for $V_1$, we choose $s=1,t=2$ and for $V_2$, we choose $s'=3,t'=4$.

As a linear group in $\rm{GL}(3,\mathbb{C})$, it has center

$$
\begin{align*}
C_n=
\langle
\begin{pmatrix}
\zeta_n & 0 & 0\\
0 & \zeta_n & 0\\
0 & 0 & \zeta_n
\end{pmatrix}
\rangle.
\end{align*}
$$


The Magma code is as follows:
<pre>

n:=5;
FScale:=CyclotomicField(3:Sparse:=true);
FScale:=Compositum(FScale,CyclotomicField(n^2:Sparse:=true));

F:=FScale;

Zn:=RootOfUnity(n);

s:=1;
t:=2;

G1:=MatrixGroup<3,F|
[Zn^s,0,0, 0,1,0, 0,0,1],
[1,0,0, 0,Zn^t,0, 0,0,1],
[0,0,1, 1,0,0, 0,1,0]>;

s':=3;
t':=4;

G2:=MatrixGroup<3,F|
[Zn^s',0,0, 0,1,0, 0,0,1],
[1,0,0, 0,Zn^t',0, 0,0,1],
[0,0,1, 1,0,0, 0,1,0]>;
</pre>

The Burnside Symbols are

$$
\begin{align*}
[\mathbb{P}(V_1) \circlearrowleft G]=&(1,G \circlearrowright k(x,y),())\\
&+(C_5,C_5^2/C_5 \circlearrowright k(x),(1))+(C_5,C_5^2/C_5 \circlearrowright k(x),(4))\\
&+(C_5^2,1 \circlearrowright k,((1,4),(3,1)))+(C_5^2,1 \circlearrowright k,((4,0),(4,1)))
\end{align*}
$$

where

$$
\begin{align*}
C_5=\langle
\begin{pmatrix}
\zeta_5^4 & 0 & 0\\
0 & \zeta_5^4 & 0\\
0 & 0 & 1
\end{pmatrix}
\rangle, 
C_5^2=\langle
\begin{pmatrix}
\zeta_5^3 & 0 & 0\\
0 & \zeta_5^4 & 0\\
0 & 0 & 1
\end{pmatrix},
\begin{pmatrix}
\zeta_5 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{pmatrix}
\rangle
\end{align*}
$$

There are conjugation relations:

$$
\begin{align*}
&(C_5^2,1 \circlearrowright k,((1,4),(3,1)))=(C_5^2,1 \circlearrowright k,((1,0),(1,4)))=(C_5^2,1 \circlearrowright k,((1,0),(3,1))),\\
&(C_5^2,1 \circlearrowright k,((4,0),(4,1)))=(C_5^2,1 \circlearrowright k,((2,4),(4,0)))=(C_5^2,1 \circlearrowright k,((2,4),(4,1))).
\end{align*}
$$



$$
\begin{align*}
[\mathbb{P}(V_2) \circlearrowleft G]=&(1,G \circlearrowright k(x,y),())\\
&+(C_5,C_5^2/C_5 \circlearrowright k(x),(2))+(C_5,C_5^2/C_5 \circlearrowright k(x),(3))\\
&+(C_5^2,1 \circlearrowright k,((3,3),(4,2)))+(C_5^2,1 \circlearrowright k,((2,0),(2,2)))
\end{align*}
$$

where

$$
\begin{align*}
C_5=\langle
\begin{pmatrix}
1 & 0 & 0\\
0 & \zeta_5^2 & 0\\
0 & 0 & 1
\end{pmatrix}
\rangle, 
C_5^2=\langle
\begin{pmatrix}
1 & 0 & 0\\
0 & \zeta_5^3 & 0\\
0 & 0 & \zeta_5
\end{pmatrix},
\begin{pmatrix}
\zeta_5^2 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{pmatrix}
\rangle
\end{align*}
$$

There are conjugation relations:

$$
\begin{align*}
&(C_5^2,1 \circlearrowright k,((3,3),(4,2)))=(C_5^2,1 \circlearrowright k,((3,0),(3,3)))=(C_5^2,1 \circlearrowright k,((3,0),(4,2))),\\
&(C_5^2,1 \circlearrowright k,((2,0),(2,2)))=(C_5^2,1 \circlearrowright k,((1,3),(2,0)))=(C_5^2,1 \circlearrowright k,((1,3),(2,2))).
\end{align*}
$$

Now if we fix generator for $C_5=\langle (g_{n,s}^1)^t(g_{n,t}^2)^s\rangle$ and $C_5^2=\langle g_{n,s}^1,g_{n,t}^2\rangle$. Two Burnside Symbols are

$$
\begin{align*}
[\mathbb{P}(V_1) \circlearrowleft G]=&(1,G \circlearrowright k(x,y),())\\
&+(C_5,C_5^2/C_5 \circlearrowright k(x),(2))+(C_5,C_5^2/C_5 \circlearrowright k(x),(3))\\
&+(C_5^2,1 \circlearrowright k,((0,3),(1,0)))+(C_5^2,1 \circlearrowright k,((0,2),(4,0)))
\end{align*}
$$

$$
\begin{align*}
[\mathbb{P}(V_2) \circlearrowleft G]=&(1,G \circlearrowright k(x,y),())\\
&+(C_5,C_5^2/C_5 \circlearrowright k(x),(2))+(C_5,C_5^2/C_5 \circlearrowright k(x),(3))\\
&+(C_5^2,1 \circlearrowright k,((0,1),(3,0)))+(C_5^2,1 \circlearrowright k,((0,4),(2,0)))
\end{align*}
$$

The combinatorial Burnside group of $C_5^2:C_3$ is
$$
\begin{align*}
\mathcal{BC}_2(C_5^2:C_3)=(\mathbb{Z}/2)^2 \times (\mathbb{Z}/30)^2 \times \mathbb{Z}^{19}
\end{align*}
$$

Remark: we don't consider symbols with trivial stabilizer group in the computation of $\mathcal{BC}$.


Let $T_2^{1,2},T_{30}^{1,2}$ and $e_i$, $i=1,\dots,19$ be the generators for $(\mathbb{Z}/2)^2$, $(\mathbb{Z}/30)^2$ and the torsion-free part respectively. 

The difference of images of two Burnside symbols $[\mathbb{P}(V_1) \circlearrowleft G]-[\mathbb{P}(V_2) \circlearrowleft G]$ under the map $\rm{Burn}_2(G) \to \mathcal{BC}_2(G)$ is:

$$
\begin{align*}
T_2^2+13T_{30}^2+e_3-e_7+e_8+2e_{11}-e_{12}+e_{16}\neq 0
\end{align*}
$$

Thus two actions are not birational to each other.