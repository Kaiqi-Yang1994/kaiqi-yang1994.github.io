---
permalink: /projects/ConicBundle/Instructions
title: "Potentially stably rational conic bundle"
author_profile: true
---


### Take group $W(D_4)$ as example.

### Copy representation of $W(D_4)$ from <a href="http://kaiqi-yang1994.github.io/files/ConicBundle/Representations.txt" target="_blank" rel="noopener noreferrer">this file</a>.

### Copy every thing from <a href="http://kaiqi-yang1994.github.io/files/ConicBundle/ConicBundleCode.txt" target="_blank" rel="noopener noreferrer">this file</a>.

### Use the following code:
<pre>

//For D4

//Get Exceptional set
Mod:=GModule(GroupD4);
u:=Mod![0,0,1,0,0,0,0,0,0,0,0];
Exceptional:=Orbit(TransGroup(GroupD4),u);
Exceptional:=SetToIndexedSet(Exceptional);

//find minimal group with every subgroup having trivial H1

ListD4:=Subgroups(GroupD4);
WantD4:={};

Total:={@ Integers() | x : x in [2..#ListD4] @};
Del:={};
for i in [2..#ListD4] do
	i;
	if i in Del eq false then
		List:=Subgroups(ListD4[i]`subgroup);
		Sum:=0;
		for j in [2..#List] do
			M:=GModule(List[j]`subgroup);
			C0:=C0Matrix(M);
			C1:=C1Matrix(M);
			H1:=quo<Nullspace(C1)|RowSpace(C0)>;
			Sum:=Sum+#H1;
		end for;
		if Sum ne #List-1 then
			Include(~Del,i);
			for j in [2..#ListD4] do
				if j in Del eq false then
					if ListD4[i]`subgroup subset ListD4[j]`subgroup then
						Include(~Del,j);
					end if;
				end if;
			end for;
		end if;
	end if;
end for;

Remain:=Total diff Del;


for i in [2..#Remain] do
	i;
	if IsMinimalInv(ListD4[Remain[i]]`subgroup,GroupD4) then
		Include(~WantD4,Remain[i]);
	end if;
end for;
WantD4;
</pre>

### All indices of the group is stored in WantD4, for other cases, change the variables name accordingly.

### We have $WantD4={30}$, and group ListD4[30]`subgroup is $S_3$.

### Use the following code to see the orbit decomposition, intersection matrix and stabilizer of each orbit.
<pre>
ReadResult(ListD4[30]`subgroup,Exceptional);
</pre>
