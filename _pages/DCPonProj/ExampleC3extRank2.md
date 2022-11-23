---
permalink: /projects/DCPonProj/C3extRank2
title: "Example $C_n^2:C_3$"
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
\begin{pmatrix}
\zeta_n^s & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{pmatrix},
\begin{pmatrix}
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
0 & 0 & 1
\end{pmatrix}
\rangle.
\end{align*}
$$


The Magma code is as follows:
<pre>

n:=5;
FScale:=CyclotomicField(3);
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
[\mathbb{P}(V_1) \circlearrowleft G]=
\end{align*}
$$

and 

$$
\begin{align*}
[\mathbb{P}(V_2) \circlearrowleft G]=
$$
