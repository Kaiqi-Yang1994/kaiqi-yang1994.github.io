---
permalink: /projects/DCPonProj/C3extRank2mn
title: "Example (C_m*C_n):C_3"
author_profile: true
---

Group $G=(C_m \oplus C_n):C_3$ is described by the short exact sequence

$$
\begin{align*}
1 \to C_m \oplus C_n \to G \to C_3 \to 1
\end{align*}
$$

When $n=14, m=2$, group $G=C_7:A_4$.

$$
\begin{align*}
G=
\langle
g_{m,r}=\begin{pmatrix}
\zeta_m^r & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{pmatrix},
g_{n,s,t}=\begin{pmatrix}
\zeta_n^s & 0 & 0\\
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

There are two representation $V_1,V_2$ of $G$, for $V_1$, we choose $s=3,r=t=1$ and for $V_2$, we choose $s'=5,r'=t'=1$.

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
m:=2;
d:=7;
n:=m*d;


FScale:=CyclotomicField(3:Sparse:=true);
FScale:=Compositum(FScale,CyclotomicField(n:Sparse:=true));

F:=FScale;

Zm:=RootOfUnity(m);
Zn:=RootOfUnity(n);

s:=3;
r:=1;
t:=1;

G1:=MatrixGroup<3,F|
[Zm^r,0,0, 0,1,0, 0,0,1],
[Zn^s,0,0, 0,Zn^t,0, 0,0,1],
[0,0,1, 1,0,0, 0,1,0]>;

s':=5;
r':=1;
t':=1;

G2:=MatrixGroup<3,F|
[Zm^(r'),0,0, 0,1,0, 0,0,1],
[Zn^(s'),0,0, 0,Zn^(t'),0, 0,0,1],
[0,0,1, 1,0,0, 0,1,0]>;

</pre>

The Burnside Symbols are

$$
\begin{align*}
[\mathbb{P}(V_1) \circlearrowleft G]=&(1,G \circlearrowright k(x,y),())\\
&+2(C_2,C_{14} \circlearrowright k(x),(1))\\
&+(C_2\times C_{14},1 \circlearrowright k,((1,5),(1,6)))+(C_2\times C_{14},1 \circlearrowright k,((0,11),(1,9)))
\end{align*}
$$

where

$$
\begin{align*}
C_2=\langle
\begin{pmatrix}
1 & 0 & 0\\
0 & -1 & 0\\
0 & 0 & 1
\end{pmatrix}
\rangle, 
C_2\times C_{14}=\langle
\begin{pmatrix}
-1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{pmatrix},
\begin{pmatrix}
-\zeta_7 & 0 & 0\\
0 & -\zeta_7^5 & 0\\
0 & 0 & 1
\end{pmatrix}
\rangle
\end{align*}
$$

There are conjugation relations:

$$
\begin{align*}
&(C_2\times C_{14},1 \circlearrowright k,((1,5),(1,6)))=(C_2\times C_{14},1 \circlearrowright k,((0,3),(1,6)))=(C_2\times C_{14},1 \circlearrowright k,((0,3),(1,5))),\\
&(C_2\times C_{14},1 \circlearrowright k,((0,11),(1,9)))=(C_2\times C_{14},1 \circlearrowright k,((1,8),(1,9)))=(C_2\times C_{14},1 \circlearrowright k,((0,11),(1,8))).
\end{align*}
$$



$$
\begin{align*}
[\mathbb{P}(V_2) \circlearrowleft G]=&(1,G \circlearrowright k(x,y),())\\
&+2(C_2,C_{14} \circlearrowright k(x),(1))\\
&+(C_2\times C_{14},1 \circlearrowright k,((1,5),(1,10)))+(C_2\times C_{14},1 \circlearrowright k,((0,1),(1,4)))
\end{align*}
$$

where

$$
\begin{align*}
C_2=\langle
\begin{pmatrix}
1 & 0 & 0\\
0 & -1 & 0\\
0 & 0 & 1
\end{pmatrix}
\rangle, 
C_2 \times C_{14}=\langle
\begin{pmatrix}
-1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{pmatrix},
\begin{pmatrix}
-\zeta_7^6 & 0 & 0\\
0 & -\zeta_7^4 & 0\\
0 & 0 & 1
\end{pmatrix}
\rangle
\end{align*}
$$

There are conjugation relations:

$$
\begin{align*}
&(C_2\times C_{14},1 \circlearrowright k,((1,5),(1,10)))=(C_2\times C_{14},1 \circlearrowright k,((0,13),(1,10)))=(C_2\times C_{14},1 \circlearrowright k,((0,13),(1,5))),\\
&(C_2\times C_{14},1 \circlearrowright k,((0,1),(1,4)))=(C_2\times C_{14},1 \circlearrowright k,((0,1),(1,9)))=(C_2\times C_{14},1 \circlearrowright k,((1,4),(1,9))).
\end{align*}
$$

Now if we fix generator for $C_2 \times C_{14}=\langle g_{m,r}^1,g_{n,s,t}^2\rangle$. Two Burnside Symbols are

$$
\begin{align*}
[\mathbb{P}(V_1) \circlearrowleft G]=&(1,G \circlearrowright k(x,y),())\\
&+2(C_2,C_{14} \circlearrowright k(x),(1))\\
&+(C_2\times C_{14},1 \circlearrowright k,((1,2),(1,11)))+(C_2\times C_{14},1 \circlearrowright k,((1,3),(1,12)))
\end{align*}
$$

$$
\begin{align*}
[\mathbb{P}(V_2) \circlearrowleft G]=&(1,G \circlearrowright k(x,y),())\\
&+2(C_2,C_{14} \circlearrowright k(x),(1))\\
&+(C_2\times C_{14},1 \circlearrowright k,((1,5),(1,10)))+(C_2\times C_{14},1 \circlearrowright k,((1,4),(1,9)))
\end{align*}
$$

The combinatorial Burnside group of $C_7:A_4$ is
$$
\begin{align*}
\mathcal{BC}_2(C_7:A_4)=(\mathbb{Z}/2)^{16} \times \mathbb{Z}/6 \times (\mathbb{Z}/12)^2 \times \mathbb{Z}/72 \times \mathbb{Z}^{21}
\end{align*}
$$

Remark: we don't consider symbols with trivial stabilizer group in the computation of $\mathcal{BC}$.


Let $T_2^{1,\dots,16},T_{6},T_{12}^{1,2},T_{72}$ and $e_i$, $i=1,\dots,21$ be the generators for $(\mathbb{Z}/2)^{16}$, $\mathbb{Z}/6$, $(\mathbb{Z}/12)^2$, $\mathbb{Z}/72$ and the torsion-free part respectively. 

The difference of images of two Burnside symbols $[\mathbb{P}(V_1) \circlearrowleft G]-[\mathbb{P}(V_2) \circlearrowleft G]$ under the map $\rm{Burn}_2(G) \to \mathcal{BC}_2(G)$ is:

$$
\begin{align*}
4T_{12}^1+56T_{72} \neq 0
\end{align*}
$$

Thus two actions are not birational to each other.