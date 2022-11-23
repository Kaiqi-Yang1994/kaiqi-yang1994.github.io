---
permalink: /projects/DCPonProj/ExamplePSL(2,7)
title: "Example PSL(2,7)"
author_profile: true
---

Group $G=\rm{PSL}(2,7)$ has 2 3-dimensional faithful representation $V_1,V_2$.

Two representations are given as follows:

$$
\begin{align*}
\mathbb{P}(V_1)=
\langle
\begin{pmatrix}
0 & 1 & 0\\
0 & 0 & 1\\
1 & 0 & 0
\end{pmatrix},
\frac{1}{i\sqrt{7}}
\begin{pmatrix}
\zeta_7^3-\zeta_7^4 & \zeta_7^5-\zeta_7^2 & \zeta_7^6-\zeta_7\\
\zeta_7^5-\zeta_7^2 & \zeta_7^6-\zeta_7 & \zeta_7^3-\zeta_7^4\\
\zeta_7^6-\zeta_7 & \zeta_7^3-\zeta_7^4 & \zeta_7^5-\zeta_7^2\\
\end{pmatrix},
\begin{pmatrix}
\zeta_7 & 0 & 0\\
0 & \zeta_7^2 & 0\\
0 & 0 & \zeta_7^4
\end{pmatrix}
\rangle
\end{align*}
$$

where $\zeta_7$ is a 7-th root of unity.

The Magma code is as follows:
<pre>

FScale:=CyclotomicField(84);

F:=FScale;

Z7:=RootOfUnity(7);
a:=Z7^4-Z7^3;
b:=Z7^2-Z7^5;
c:=Z7-Z7^6;
isq7:= 2*Z7^4 + 2*Z7^2 + 2*Z7 + 1;

G:=MatrixGroup<3,F|
[0,1,0, 0,0,1, 1,0,0],
[-a/isq7,-b/isq7,-c/isq7, -b/isq7,-c/isq7,-a/isq7, -c/isq7,-a/isq7,-b/isq7],
[Z7,0,0, 0,Z7^2,0, 0,0,Z7^4]>;

</pre>

$$
\begin{align*}
\mathbb{P}(V_2)=
\langle
\begin{pmatrix}
0 & 1 & 0\\
0 & 0 & 1\\
1 & 0 & 0
\end{pmatrix},
\frac{1}{i\sqrt{7}}
\begin{pmatrix}
\zeta_7^3-\zeta_7^4 & \zeta_7^5-\zeta_7^2 & \zeta_7^6-\zeta_7\\
\zeta_7^5-\zeta_7^2 & \zeta_7^6-\zeta_7 & \zeta_7^3-\zeta_7^4\\
\zeta_7^6-\zeta_7 & \zeta_7^3-\zeta_7^4 & \zeta_7^5-\zeta_7^2\\
\end{pmatrix},
\begin{pmatrix}
\zeta_7^3 & 0 & 0\\
0 & \zeta_7^6 & 0\\
0 & 0 & \zeta_7^5
\end{pmatrix}
\rangle
\end{align*}
$$

where $\zeta_7$ is a 7-th root of unity.

The Magma code is as follows:
<pre>

FScale:=CyclotomicField(84);

F:=FScale;

Z7:=RootOfUnity(7);
a:=Z7^4-Z7^3;
b:=Z7^2-Z7^5;
c:=Z7-Z7^6;
isq7:= 2*Z7^4 + 2*Z7^2 + 2*Z7 + 1;

G:=MatrixGroup<3,F|
[0,1,0, 0,0,1, 1,0,0],
[-a/isq7,-b/isq7,-c/isq7, -b/isq7,-c/isq7,-a/isq7, -c/isq7,-a/isq7,-b/isq7],
[Z7^3,0,0, 0,Z7^6,0, 0,0,Z7^5]>;

</pre>


The Burnside Symbols are

$$
\begin{align*}
[\mathbb{P}(V_1) \circlearrowleft G]=&(1,G \circlearrowright k(x,y),())\\
&+(C_2, C_2^2\circlearrowright k(x),(1))+(C_3,1 \circlearrowright k,(1,1))\\
&+(C_7,1 \circlearrowright k,(3,6))+(C_7,1 \circlearrowright k,(1,2))\\
&+(1.C_2^2,1 \circlearrowright k,((0,1),(1,0)))+(2.C_2^2,1 \circlearrowright k,((0,1),(1,0)))\\
&+(C_4,1 \circlearrowright k,(1,1))+(C_4,1 \circlearrowright k,(2,3))
\end{align*}
$$

where

$$
\begin{align*}
C_2=\langle
\frac{1}{7}
\begin{pmatrix}
-2\zeta_{84}^{22}+3\zeta_{84}^{16}-3\zeta_{84}^{12}+2\zeta_{84}^{8}+2\zeta_{84}^{6}-3\zeta_{84}^{2}-4 & 4\zeta_{84}^{22}-\zeta_{84}^{18}-\zeta_{84}^{16}+4\zeta_{84}^{12}-4\zeta_{84}^{8}-2\zeta_{84}^{6}+\zeta_{84}^{2}+2 & 2\zeta_{84}^{18}+4\zeta_{84}^{16}-3\zeta_{84}^{12}+3\zeta_{84}^{6}-4\zeta_{84}^2-2\\
\zeta_{84}^{22}+\zeta_{84}^{18}-3\zeta_{84}^{16}-\zeta_{84}^8-3\zeta_{84}^6+3\zeta_{84}^2+1 & 3\zeta_{84}^{22}-\zeta_{84}^{16}+\zeta_{84}^{12}-3\zeta_{84}^8-3\zeta_{84}^6+\zeta_{84}^2-1 & -3\zeta_{84}^{22}+3\zeta_{84}^{18}-2\zeta_{84}^{12}+3\zeta_{84}^8+4\zeta_{84}^6-2\\
-\zeta_{84}^{22}-2\zeta_{84}^{18}+\zeta_{84}^{16}-2\zeta_{84}^{12}+\zeta_{84}^8-2\zeta_{84}^6-\zeta_{84}^2 & -\zeta_{84}^{22}-3\zeta_{84}^{18}-\zeta_{84}^{16}+3\zeta_{84}^{12}+\zeta_{84}^8+\zeta_{84}^2+1 & -\zeta_{84}^{22}-2\zeta_{84}^{16}+2\zeta_{84}^{12}+\zeta_{84}^8+\zeta_{84}^6+2\zeta_{84}^2-2
\end{pmatrix}
\rangle
\end{align*}
$$

The action on $\mathbb{P}^1$ is given by
$$
\begin{align*}
C_2^2=
\langle
&\frac{1}{7}
\begin{pmatrix}
-3\zeta_{84}^{22}+2\zeta_{84}^{18}+5\zeta_{84}^{16}-4\zeta_{84}^{12}+3\zeta_{84}^8-\zeta_{84}^6-5\zeta_{84}^2-1 & -\zeta_{84}^{22}-4\zeta_{84}^{18}+4\zeta_{84}^{16}+\zeta_{84}^{12}+\zeta_{84}^8+2\zeta_{84}^6-4\zeta_{84}^2-5\\
-5\zeta_{84}^{22}+\zeta_{84}^18+6\zeta_{84}^{16}-9\zeta_{84}^{12}+5\zeta_{84}^8+3\zeta_{84}^6-6\zeta_{84}^2-4 & 3\zeta_{84}^{22}-2\zeta_{84}^{18}-5\zeta_{84}^{16}+4\zeta_{84}^{12}-3\zeta_{84}^8+\zeta_{84}^6+5\zeta_{84}^2+1
\end{pmatrix},\\
&\frac{1}{7}
\begin{pmatrix}
2\zeta_{84}^{22}-6\zeta_{84}^{18}-\zeta_{84}^{16}+5\zeta_{84}^{12}-2\zeta_{84}^8-4\zeta_{84}^6+\zeta_{84}^2+3 & -4\zeta_{84}^{22}-2\zeta_{84}^{18}+2\zeta_{84}^{16}+4\zeta_{84}^{12}+4\zeta_{84}^8+\zeta_{84}^6-2\zeta_{84}^2+1\\
8\zeta_{84}^{22}-3\zeta_{84}^{18}-4\zeta_{84}^{16}+6\zeta_{84}^{12}-8\zeta_{84}^8-2\zeta_{84}^6+4\zeta_{84}^2-2 & -2\zeta_{84}^{22}+6\zeta_{84}^{18}+\zeta_{84}^{16}-5\zeta_{84}^{12}+2\zeta_{84}^8+4\zeta_{84}^6-\zeta_{84}^2-3
\end{pmatrix}
\rangle
\end{align*}
$$

$$
\begin{align*}
C_3=
\langle
\begin{pmatrix}
0 & 0 & \zeta_{84}^{22}-\zeta_{84}^8\\
-\zeta_{84}^{16}+\zeta_{84}^2 & 0 & 0\\
0 & -\zeta_{84}^{18} & 0
\end{pmatrix}
\rangle,
C_7=
\langle
\begin{pmatrix}

\end{pmatrix}
\rangle
\end{align*}
$$

