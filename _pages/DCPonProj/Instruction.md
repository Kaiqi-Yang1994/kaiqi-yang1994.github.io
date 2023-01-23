---
permalink: /projects/DCPonProj/Instructions
title: "Projects"
author_profile: true
---
Given a representation $\Phi$ of a group $G \subset PGL_{n+1}$ acting on $\mathbb{P}^n$, follow the instructions to compute the Burnside symbols.

<ol type="1">

<li>Copy all lines from <a href="http://kaiqi-yang1994.github.io/files/DCPonProj/DCPonProj.txt">Magma code</a>.</li>

<li>Input 3 entries:
	<ul>
	<li>$FScale$, a cyclotomic field which contains eigenvalues of all elements in $\Phi(G)$.</li>
	<li>$F$, extension of $FScale$, such that the representation of $\Phi(G)$ is defined over $F$.</li>
 	<li>$\Phi(G)$, a matrix group defined over $F$.</li>
	</ul>
</li>

<li>To compute Burnside symbols, use command
<pre>
<small>
BurnsideSymbols,PG2GHom,G2PGHom,PermG,H,LH,GrpQuo,AllGrp,ChainNode,ChainClass,<br>
ScalarGrp,AllSymbolNGLambda:=ComputeBurnsideSymbol(G,F,FScale);
</small>
</pre>
It will computes the Burnside symbols, display the simplified version of Burnside symbols and computes the conjugated $\beta$ under the action of normalizer of stabilizer of the corresponding symbol.
</li>

<li>To check the simplified version of BurnsideSymbols again, use command
<pre>
ReadBurnsideSymbols(BurnsideSymbols);
</pre>
</li>

<li>To check the conjugated $\beta$ again, use command
<pre>
EquivSymbols:=FindEquivSymbol(BurnsideSymbols,H);
for i in [1..#EquivSymbols] do
	EquivSymbols[i];
end for;
</pre>
</li>

</ol>
