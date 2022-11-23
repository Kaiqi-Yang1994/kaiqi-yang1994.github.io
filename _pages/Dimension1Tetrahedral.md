---
permalink: /projects/DCPonProj/ProjLinGrpDim1/Tetrahedral
title: "Dimension1 Tetrahedral"
author_profile: true
---

Group $G=A_4$ does not have 2-dimensional representation, its binary-extension $SL(2,3)$ has 3 2-dimensional representation, one representation is as follows:

$$
\begin{align*}
G=\langle
\begin{pmatrix}
\zeta_4 & 0\\
0 & \zeta_4^{-1}
\end{pmatrix},
\begin{pmatrix}
0 & 1\\
-1 & 0
\end{pmatrix},
\begin{pmatrix}
(1+\zeta_4)/2 & (-1+\zeta_4)/2\\
(1+\zeta_4)/2 & (1-\zeta_4)/2
\end{pmatrix}
\rangle.
\end{align*}
$$

where $\zeta_4$ is a 4-th root of unity.

The Magma code is as follows:
<pre>

FScale:=CyclotomicField(24:Sparse:=true);

F:=FScale;

Z4:=RootOfUnity(4);

G:=MatrixGroup<2,F|
[Z4,0, 0,Z4^(-1)],
[0,1, -1,0],
[(1+Z4)/2,(-1+Z4)/2, (1+Z4)/2,(1-Z4)/2]>;

</pre>

The Burnside symbol is

$$
\begin{align*}
[\mathbb{P}^1 \circlearrowleft G]=&(1,G \circlearrowright k(x),())\\
&+(C_2,1 \circlearrowright k,(1))\\
&+(C_3,1 \circlearrowright k,(1))+(C_3,1 \circlearrowright k,(2))
\end{align*}
$$

where

$$
\begin{align*}
C_2=\langle
\begin{pmatrix}
0 & i\\
i & 0
\end{pmatrix}
\rangle,
C_3=\langle
\begin{pmatrix}
(1+\zeta_4)/2 & (-1+\zeta_4)/2\\
(1+\zeta_4)/2 & (1-\zeta_4)/2
\end{pmatrix}
\rangle
\end{align*}
$$

The other 2 projective linear representation of $A_4$ gives the same Burnside symbols.