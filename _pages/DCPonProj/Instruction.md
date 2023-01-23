---
permalink: /projects/DCPonProj/Instruction
title: "Projects"
author_profile: true
---
Given a representation $\Phi$ of a group $G \subset PGL_{n+1}$ acting on $\mathbb{P}^n$, follow the instructions to compute the Burnside symbols.

<ul type="1">
<li>Copy all lines from <a href="http://kaiqi-yang1994.github.io/files/DCPonProj/DCPonProj.txt">Magma code</a>.</li>
<li>Input 3 entries:
	<ul>
	<li>$FScale$, a cyclotomic field which contains eigenvalues of all elements in $\Phi(G)$.</li>
	<li>$F$, extension of FScale, such that the representation of $\Phi(G)$ is defined over $F$.</li>
 	<li>$\Phi(G)$, a matrix group defined over $F$.</li>
</ul>
