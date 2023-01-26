---
permalink: /projects/DCPonProj/D5timesD4
title: "Example D5*D4"
author_profile: true
---

Group $D_5 \times D_4$ has two representation $V_1,V_2$.

Representation $V_1$ is given as follows:
$$
\begin{align*}
G_1=\langle
\begin{pmatrix}
0 & 1 & 0 & 0\\
1 & 0 & 0 & 0\\
0 & 0 & 1 & 0\\
0 & 0 & 0 & 1
\end{pmatrix},
\begin{pmatrix}
\zeta_5 & 0 & 0 & 0\\
0 & \zeta_5^{-1} & 0 & 0\\
0 & 0 & 1 & 0\\
0 & 0 & 0 & 1
\end{pmatrix},
\begin{pmatrix}
1 & 0 & 0 & 0\\
0 & 1 & 0 & 0\\
0 & 0 & 0 & 1\\
0 & 0 & 1 & 0
\end{pmatrix},
\begin{pmatrix}
1 & 0 & 0 & 0\\
0 & 1 & 0 & 0\\
0 & 0 & \zeta_4 & 0\\
0 & 0 & 0 & \zeta_4^{-1}
\end{pmatrix},
\rangle
\end{align*}
$$


The Magma code is
<pre>
FScale:=CyclotomicField(40:Sparse:=true);

F:=FScale;

Z5:=RootOfUnity(5);
Z4:=RootOfUnity(4);

G:=MatrixGroup<4,F|
[0,1,0,0, 1,0,0,0, 0,0,1,0, 0,0,0,1],
[Z5,0,0,0, 0,Z5^(-1),0,0, 0,0,1,0, 0,0,0,1],
[1,0,0,0, 0,1,0,0, 0,0,0,1, 0,0,1,0],
[1,0,0,0, 0,1,0,0, 0,0,Z4,0, 0,0,0,Z4^(-1)]>;
</pre>


The Burnside symbols are in Magma state file.

Another representation $V_2$ is given as follows:

$$
\begin{align*}
G_2=\langle
\begin{pmatrix}
0 & 1 & 0 & 0\\
1 & 0 & 0 & 0\\
0 & 0 & 1 & 0\\
0 & 0 & 0 & 1
\end{pmatrix},
\begin{pmatrix}
\zeta_5^2 & 0 & 0 & 0\\
0 & \zeta_5^{-2} & 0 & 0\\
0 & 0 & 1 & 0\\
0 & 0 & 0 & 1
\end{pmatrix},
\begin{pmatrix}
1 & 0 & 0 & 0\\
0 & 1 & 0 & 0\\
0 & 0 & 0 & 1\\
0 & 0 & 1 & 0
\end{pmatrix},
\begin{pmatrix}
1 & 0 & 0 & 0\\
0 & 1 & 0 & 0\\
0 & 0 & \zeta_4 & 0\\
0 & 0 & 0 & \zeta_4^{-1}
\end{pmatrix},
\rangle
\end{align*}
$$


The Magma code is
<pre>
FScale:=CyclotomicField(40:Sparse:=true);

F:=FScale;

Z5:=RootOfUnity(5);
Z4:=RootOfUnity(4);

G:=MatrixGroup<4,F|
[0,1,0,0, 1,0,0,0, 0,0,1,0, 0,0,0,1],
[Z5^2,0,0,0, 0,Z5^(-2),0,0, 0,0,1,0, 0,0,0,1],
[1,0,0,0, 0,1,0,0, 0,0,0,1, 0,0,1,0],
[1,0,0,0, 0,1,0,0, 0,0,Z4,0, 0,0,0,Z4^(-1)]>;
</pre>


The Burnside symbols are in Magma state file.