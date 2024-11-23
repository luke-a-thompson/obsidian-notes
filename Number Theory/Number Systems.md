A set $S$ is closed under an operation $\cdot$ $S$ if all pairs produce a result $\in S$:
$$
\forall a,b \in S, a\cdot b \in S
$$$S$ is *not closed* under $\cdot$ if any pair produces a result $\notin S$:
$$
\exists a,b \in S, a \cdot b \notin S
$$
Hence, proof of closure requires proof for all elements, while proof of non-closure only requires a single counterexample.

## Overview of Key Properties
There is a strict subset relationship such that:
$$
\mathbb{N} \subsetneq \mathbb{Q} \subsetneq \mathbb{R}
$$
$\mathbb{N}, \mathbb{Z}, \mathbb{Q}$ are countable. $\mathbb{R}$ is uncountable.
$\mathbb{Q}$ is dense in $\mathbb{R}$. Between any two $\forall a,b \in \mathbb{R}: a<b \implies \forall q \in \mathbb{Q}: a < q < b$.
* Even at a small interval like 1.00 and 1.01, there are rational numbers between

## Natural Numbers $\mathbb{N}$
$$
\mathbb{N} = \{1,2,3,\dots \}
$$Closed under:
* Addition: (e.g., $3+2=5 \in \mathbb{N}$)
* Multiplication (e.g., $3\times2=6\in \mathbb{N}$)
Not closed under:
* Subtraction (e.g., $2-3=-1\notin \mathbb{N}$)
* Division (e.g., $\frac{1}{2}=0.5\notin \mathbb{N}$)

## Integers $\mathbb{Z}$
$$
\mathbb{Z}= \{\dots,-2,-1,0,1,2,\dots,\}
$$
Closed under:
* Addition: (e.g., $-3+2=-1 \in \mathbb{Z}$)
* Subtraction: (e.g., $4-6=-2 \in \mathbb{Z}$)
* Multiplication: (e.g., $-3 \times 2 = -6 \in \mathbb{Z}$)
Not closed under:
* Division: (e.g., $\frac{1}{2}=0.5 \notin \mathbb{Z}$)

## Rational Numbers $\mathbb{Q}$
$$
\mathbb{Q} = \{\frac{p}{q}\space|\space p,q \in \mathbb{Z}, q \neq 0\}
$$Recall that $|$ means such that. Hence, the rationals $\mathbb{Q}$ are any numbers who can be represented as a fraction of integers $\mathbb{Z}$.

Closed under:
* Addition (e.g.,$\frac{1}{2}+\frac{2}{3}=\frac{7}{6}\in \mathbb{Q}$)
* Subtraction (e.g., $\frac{1}{2}-\frac{2}{3}=-\frac{1}{6} \in \mathbb{Q}$)
* Multiplication (e.g., $\frac{1}{2}\times \frac{2}{3}=\frac{1}{3} \in \mathbb{Q}$)
* Division (e.g., e.g., $\frac{1}{2}\div\frac{2}{3}=-\frac{3}{4} \in \mathbb{Q}$)

Properties:
* Countable: $\mathbb{N} \rightarrow \mathbb{Q}$
* Not complete: The [[Cauchy Sequence]] may converge to a limit $L \not\in \mathbb{Q}$
	* E.g., The sequence ${x_{n}=1,1.4,1.41,1.414}$ (approximations of $\sqrt{ 2 }$) is a [[Cauchy Sequence]], but does not converge to a $\mathbb{Q}$

## Real Numbers $\mathbb{R}$

Closed under:
* Addition (e.g., $\pi +2 \in \mathbb{R}$)
* Subtraction (e.g., $\sqrt{2}-1 \in \mathbb{R}$)
* Multiplication (e.g., $\pi \times \sqrt{2} \in \mathbb{R}$)
* Division (e.g., $\frac{\pi}{\sqrt{2}} \in \mathbb{R}$)
