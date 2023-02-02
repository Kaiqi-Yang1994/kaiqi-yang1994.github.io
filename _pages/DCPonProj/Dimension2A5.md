---
permalink: /projects/DCPonProj/ProjLinGrpDim2/A5
title: "Dimension2 A5"
author_profile: true
---

Group $G=A_5$ has 2 3-dimensional representations, one representation is as follows:

$$
\begin{align*}
G=\langle
\begin{pmatrix}
1 & 0 & 0\\
0 & \zeta_5^4 & 0\\
0 & 0 & \zeta_5
\end{pmatrix},
\begin{pmatrix}
-1 & 0 & 0\\
0 & 0 & -1\\
0 & -1 & 0
\end{pmatrix},
\frac{1}{\sqrt{5}}
\begin{pmatrix}
1 & 1 & 1\\
2 & s & t\\
2 & t & s
\end{pmatrix}
\rangle.
\end{align*}
$$

where $\zeta_5$ is a 5-th root of unity, $s=\zeta_5^2+\zeta_5^3$ and $t=\zeta_5+\zeta_5^4$.

The Magma code is as follows:
<pre>

FScale:=CyclotomicField(60);

F:=FScale;

Z5:=RootOfUnity(5);
s:=Z5^2+Z5^3;
t:=Z5+Z5^4;
sq5:=2*t+1;


G:=MatrixGroup<3,F|
[1,0,0, 0,Z5^4,0, 0,0,Z5],
[-1,0,0, 0,0,-1, 0,-1,0],
[1/sq5,1/sq5,1/sq5, 2/sq5,s/sq5,t/sq5, 2/sq5,t/sq5,s/sq5]>;

</pre>

The Burnside symbol is

$$
\begin{align*}
[\mathbb{P}^2 \circlearrowleft G]=&(1,G \circlearrowright k(x,y),())\\
&+2(C_2,C_2 \circlearrowright k(x),(1))+(C_3,1 \circlearrowright k(x),(1,1))\\
&+(C_5,1 \circlearrowright k,(1,2))+(C_5,1 \circlearrowright k,(3,3))+(C_5,1 \circlearrowright k,(3,4))\\
&+(C_2^2,1 \circlearrowright k,((1,0),(1,1)))+(C_2^2,1 \circlearrowright k,((0,1),(1,0)))
\end{align*}
$$

For more detail, see file <a href="http://kaiqi-yang1994.github.io/files/DCPonProj/Dim2A51" download> First $A_5$</a>


Another linear representation of $A_5$ is given by

$$
\begin{align*}
G=\langle
\begin{pmatrix}
1 & 0 & 0\\
0 & \zeta_5^3 & 0\\
0 & 0 & \zeta_5^2
\end{pmatrix},
\begin{pmatrix}
-1 & 0 & 0\\
0 & 0 & -1\\
0 & -1 & 0
\end{pmatrix},
\frac{1}{\sqrt{5}}
\begin{pmatrix}
-1 & -1 & -1\\
-2 & -t & -s\\
-2 & -s & -t
\end{pmatrix}
\rangle.
\end{align*}
$$

where $\zeta_5$ is a 5-th root of unity, $s=\zeta_5^2+\zeta_5^3$ and $t=\zeta_5+\zeta_5^4$.


The Magma code is as follows:
<pre>

FScale:=CyclotomicField(60);

F:=FScale;

Z5:=RootOfUnity(5);
s:=Z5^2+Z5^3;
t:=Z5+Z5^4;
sq5:=2*t+1;


G:=MatrixGroup<3,F|
[1,0,0, 0,Z5^3,0, 0,0,Z5^2],
[-1,0,0, 0,0,-1, 0,-1,0],
[-1/sq5,-1/sq5,-1/sq5, -2/sq5,-t/sq5,-s/sq5, -2/sq5,-s/sq5,-t/sq5]>;

</pre>

The Burnside symbol is

$$
\begin{align*}
[\mathbb{P}^2 \circlearrowleft G]=&(1,G \circlearrowright k(x,y),())\\
&+2(C_2,C_2 \circlearrowright k(x),(1))+(C_3,1 \circlearrowright k(x),(2,2))\\
&+2(C_5,1 \circlearrowright k,(1,2))+(C_5,1 \circlearrowright k,(3,3))\\
&+(C_2^2,1 \circlearrowright k,((1,0),(1,1)))+(C_2^2,1 \circlearrowright k,((0,1),(1,0)))
\end{align*}
$$


For more detail, see file<a href="http://kaiqi-yang1994.github.io/files/DCPonProj/Dim2A52" download> Second $A_5$</a>

These 2 Burnside classes are the same.