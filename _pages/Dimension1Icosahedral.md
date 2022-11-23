---
permalink: /projects/DCPonProj/ProjLinGrpDim1/Icosahedral
title: "Dimension1 Icosahedral"
author_profile: true
---

Group $G=A_5$ does not have 2-dimensional representation, its binary-extension $SL(2,5)$ has 2 2-dimensional representation, one representation is as follows:

$$
\begin{align*}
G=\langle
\begin{pmatrix}
0 & 1\\
-1 & 0
\end{pmatrix},
\frac{1}{\sqrt{5}}
\begin{pmatrix}
-\zeta_5+\zeta_5^4 & \zeta_5^2-\zeta_5^3\\
\zeta_5^2-\zeta_5^3 & \zeta_5-\zeta_5^4
\end{pmatrix},
\begin{pmatrix}
\zeta_5^3 & 0\\
0 & \zeta_5^2
\end{pmatrix}
\rangle.
\end{align*}
$$

where $\zeta_5$ is a 5-th root of unity.

The Magma code is as follows:
<pre>

FScale:=CyclotomicField(60);

F:=FScale;

Z5:=RootOfUnity(5);
sq5:=2*Z5^3 + 2*Z5^2 + 1;
s:=Z5-Z5^4;
t:=Z5^2-Z5^3;


G:=MatrixGroup<2,F|
[0,1, -1,0],
[-s/sq5,t/sq5, t/sq5,s/sq5],
[Z5^3,0, 0,Z5^2]>;

</pre>

The Burnside symbol is

$$
\begin{align*}
[\mathbb{P}^1 \circlearrowleft G]=&(1,G \circlearrowright k(x),())\\
&+(C_2,1 \circlearrowright k,(1))\\
&+(C_3,1 \circlearrowright k,(2))+(C_5,1 \circlearrowright k,(3))
\end{align*}
$$

where

$$
\begin{align*}
C_2=\langle
\begin{pmatrix}
0 & \zeta_{10}^2\\
\zeta_{10}^3 & 0
\end{pmatrix}
\rangle,
C_3=\langle
\frac{1}{5}
\begin{pmatrix}
-\zeta_{60}^{14}+\zeta_{60}^{12}-2\zeta_{60}^{6}+\zeta_{60}^{4}-2 & -3\zeta_{60}^{14}-2\zeta_{60}^{12}+4\zeta_{60}^{6}+3\zeta_{60}^{4}-1\\
2\zeta_{60}^{14}-2\zeta_{60}^{12}-\zeta_{60}^{6}-2\zeta_{60}^{4}-1 & \zeta_{60}^{14}-\zeta_{60}^{12}+2\zeta_{60}^{6}-\zeta_{60}^{4}-3
\end{pmatrix}
\rangle,
C_5=\langle
\frac{1}{5}
\begin{pmatrix}
4\zeta_{60}^{14}+\zeta_{60}^{12}-2\zeta_{60}^{6}-4\zeta_{60}^{4}+3 & 2\zeta_{60}^{14}+3\zeta_{60}^{12}-\zeta_{60}^{6}-2\zeta_{60}^{4}+4\\
2\zeta_{60}^{14}+3\zeta_{60}^{12}-\zeta_{60}^{6}-2\zeta_{60}^{4}-1 & \zeta_{60}^{14}-\zeta_{60}^{12}-3\zeta_{60}^{6}-\zeta_{60}^{4}+2
\end{pmatrix}
\rangle,
\end{align*}
$$

There are conjugation relation:
$$
\begin{align*}
(C_3,1 \circlearrowright k,(1))=(C_3,1 \circlearrowright k,(2))\\
(C_5,1 \circlearrowright k,(2))=(C_5,1 \circlearrowright k,(3))
\end{align*}
$$

Another projective linear representation of $A_5$ is given by

$$
\begin{align*}
G=\langle
\begin{pmatrix}
0 & 1\\
-1 & 0
\end{pmatrix},
\frac{1}{\sqrt{5}}
\begin{pmatrix}
-\zeta_5+\zeta_5^4 & \zeta_5^2-\zeta_5^3\\
\zeta_5^2-\zeta_5^3 & \zeta_5-\zeta_5^4
\end{pmatrix},
\begin{pmatrix}
\zeta_5^1 & 0\\
0 & \zeta_5^4
\end{pmatrix}
\rangle.
\end{align*}
$$

where $\zeta_5$ is a 5-th root of unity.

The Magma code is as follows:
<pre>

FScale:=CyclotomicField(60);

F:=FScale;

Z5:=RootOfUnity(5);
sq5:=2*Z5^3 + 2*Z5^2 + 1;
s:=Z5-Z5^4;
t:=Z5^2-Z5^3;


G:=MatrixGroup<2,F|
[0,1, -1,0],
[-s/sq5,t/sq5, t/sq5,s/sq5],
[Z5^1,0, 0,Z5^4],>;

</pre>

The Burnside symbol is

$$
\begin{align*}
[\mathbb{P}^1 \circlearrowleft G]=&(1,G \circlearrowright k(x),())\\
&+(C_2,1 \circlearrowright k,(1))\\
&+(C_3,1 \circlearrowright k,(2))+(C_5,1 \circlearrowright k,(4))
\end{align*}
$$

where

$$
\begin{align*}
C_2=\langle
\begin{pmatrix}
0 & -\zeta_{10}^3\\
-\zeta_{10}^2 & 0
\end{pmatrix}
\rangle,
C_3=\langle
\frac{1}{5}
\begin{pmatrix}
-\zeta_{60}^{14}+\zeta_{60}^{12}-2\zeta_{60}^{6}+\zeta_{60}^{4}-2 & 2\zeta_{60}^{14}-2\zeta_{60}^{12}-\zeta_{60}^{6}-2\zeta_{60}^{4}-1\\
-3\zeta_{60}^{14}-2\zeta_{60}^{12}+4\zeta_{60}^{6}+3\zeta_{60}^{4}-1 & \zeta_{60}^{14}-\zeta_{60}^{12}+2\zeta_{60}^{6}-\zeta_{60}^{4}-3
\end{pmatrix}
\rangle,
C_5=\langle
\frac{1}{5}
\begin{pmatrix}
-2\zeta_{60}^{14}+2\zeta_{60}^{12}+\zeta_{60}^{6}+2\zeta_{60}^{4}+1 & -\zeta_{60}^{14}+\zeta_{60}^{12}+3\zeta_{60}^{6}+\zeta_{60}^{4}-2\\
4\zeta_{60}^{14}+\zeta_{60}^{12}-2\zeta_{60}^{6}-4\zeta_{60}^{4}+3 & -3\zeta_{60}^{14}-2\zeta_{60}^{12}+4\zeta_{60}^{6}+3\zeta_{60}^{4}-1
\end{pmatrix}
\rangle,
\end{align*}
$$

There are conjugation relation:
$$
\begin{align*}
(C_3,1 \circlearrowright k,(1))=(C_3,1 \circlearrowright k,(2))\\
(C_5,1 \circlearrowright k,(1))=(C_5,1 \circlearrowright k,(4))
\end{align*}
$$