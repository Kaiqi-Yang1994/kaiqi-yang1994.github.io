---
permalink: /projects/DCPonProj/ProjLinGrpDim1/Octahedral
title: "Dimension1 Octahedral"
author_profile: true
---

Group $G=S_4$ does not have faithful 2-dimensional representation, its binary-extension $C_2.S_4$ has 2 2-dimensional faithful representation, one representation is as follows:

$$
\begin{align*}
G=\langle
\begin{pmatrix}
\zeta_8 & 0\\
0 & \zeta_8^{-1}
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

where $\zeta_4$ is a 4-th root of unity, $\zeta_8$ is a 8-th root of unity.

The Magma code is as follows:
<pre>

FScale:=CyclotomicField(24:Sparse:=true);

F:=FScale;

Z8:=F.1;

G:=MatrixGroup<2,F|
[Z8,0, 0,Z8^(-1)],
[0,1, -1,0],
[(Z8^2+1)/2,(Z8^2-1)/2, (Z8^2+1)/2,(1-Z8^2)/2]>;

</pre>

The Burnside symbol is

$$
\begin{align*}
[\mathbb{P}^1 \circlearrowleft G]=&(1,G \circlearrowright k(x),())\\
&+(C_2,1 \circlearrowright k,(1))\\
&+(C_3,1 \circlearrowright k,(2))+(C_4,1 \circlearrowright k,(1))
\end{align*}
$$

where

$$
\begin{align*}
C_2=\langle
\begin{pmatrix}
(-\zeta_8-\zeta_8^3)/2 & (\zeta_8+\zeta_8^3)/2\\
(\zeta_8+\zeta_8^3)/2 & (\zeta_8+\zeta_8^3)/2
\end{pmatrix}
\rangle,
C_3=\langle
\begin{pmatrix}
(1-\zeta_4)/2 & (1-\zeta_4)/2\\
(-1-\zeta_4)/2 & (1+\zeta_4)/2
\end{pmatrix}
\rangle,
C_4=\langle
\begin{pmatrix}
(\zeta_8-\zeta_8^3)/2 & (\zeta_8-\zeta_8^3)/2\\
(-\zeta_8+\zeta_8^3)/2 & (\zeta_8-\zeta_8^3)/2
\end{pmatrix}
\rangle
\end{align*}
$$

There are conjugaction relations:

$$
\begin{align*}
(C_3,1 \circlearrowright k,(1))=(C_3,1 \circlearrowright k,(2))\\
(C_4,1 \circlearrowright k,(1))=(C_4,1 \circlearrowright k,(3))
\end{align*}
$$

The other projective linear representation of $S_4$ gives the same Burnside symbols.