[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/AtNXzL3S)
# Isomorphism

Prove that if two graphs $A$ and $B$ do not have the same number of nodes, they
cannot be isomorphic. I have started with the formal definition of isomorphism
below. Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$G_1=(V_1 , E_1)$ is isomorphic to $G_2 = (V_2, E_2)$ if there exists a
one-to-one and onto function (bijection) $f: V_1 \rightarrow V_2$ such that $(u,v)
\in E_1$ iff $(f(u),f(v)) \in E_2$.

For $G_1$ and $G_2$ to be isomorphic, there must exist a bijection function, denoted as $f: V(G_1) \rightarrow V(G_2)$, where $V(G_1)$ and $V(G_2)$ represent the vertex sets of $G_1$ and $G_2$ respectively. A bijection function implies a one-to-one and onto mapping.

For a one-to-one function to exist, distinct vertices from $G_1$ must map to distinct vertices in $G_2$. Formally, $\forall v, w \in V(G_1)$, if $v \neq w$, then $f(v) \neq f(w)$. This ensures that no two vertices in $G_1$ map to the same vertex in $G_2$.

For an onto function to exist, it must be possible to map all vertices in $G_2$ to a vertex in $G_1$. Formally, $\forall v \in V(G_2)$, $\exists u \in V(G_1)$ such that $f(u) = v$. This ensures that every vertex in $G_2$ has a pre-image in $G_1$ under the function $f$.

A bijection implies a one-to-one correspondence, or essentially a pairing of vertices. Now, consider $G_1$ having $n$ vertices and $G_2$ having $m$ vertices, where $m < n$. Since $G_1$ has more vertices than $G_2$, if a bijection exists, $G_2$ will run out of vertices to pair with before $G_1$ does. Consequently, $G_1$ must map its remaining vertices to non-unique vertices in $G_2$, violating the one-to-one property of the function.

Similarly, if $G_2$ has more vertices than $G_1$, the function cannot be onto since $G_1$ would run out of vertices to pair with in $G_2$. Mapping the remaining vertices of $G_2$ would make the function onto, but it would no longer be one-to-one.

Therefore, not having the same number of vertices prevents the existence of a bijection function that satisfies both the one-to-one and onto properties, which are required for isomorphism. Thus, if $G_1$ and $G_2$ do not have the same number of vertices, they cannot be isomorphic.

