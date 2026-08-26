# CS 197 WZZQ - Assessment 02

Submitted by Stephen Singer (2019-05493) on August 30, 2026.

## Growth

Consider the following functions $f_{n}$, to be organized by growth rate:
- $n^{\frac{5}{2}}$
- $\log{n^2}$
- $n^2$
- $10 \log{n^{\frac{3}{2}}}$
- $\log^2{n}$

Given two algorithms for the same problem, with time complexities $O(f_{i}(n))$ and $O(f_{{j}}(n))$,  the following holds:

1. If $\lim_{ n \to \infty } \dfrac{f_i(n)}{f_j(n)} = 0$ then $f_{i}(n) = O(f_{j}(n))$. This means $f_{i}$ grows more slowly than $f_{j}$
2. If $\lim_{ n \to \infty } \dfrac{f_i(n)}{f_j(n)} = c$, given $0 \lt c \lt \infty$, then $f_{i}(n) = \Theta(f_{j}(n))$. This means $f_{i}, f_{j}$ have the same asymptotic growth
3.  If $\lim_{ n \to \infty } \dfrac{f_i(n)}{f_j(n)} \to \infty$ then $f_{i}(n) = \Omega (f_{j}(n))$. This means $f_{i}$ grows faster than $f_{j}$

There are $\binom{5}{2}=10$ unique pair of functions $f_{i}, f_{j}$ to compare. However, the analysis can be simplified by grouping functions into the same asymptotic behavior.

The following functions
$$
	\log(n^2), \qquad 10\log(n^{3/2}), \qquad \log^2{n}
$$

can be expressed in the general form 
$$
f_{i}(n) = a \log_{b} (n^{d})^c, \quad a, b, c, d \in \mathbb{R} 
$$

### Polynomial Growth

Given $f_{i} = n^{2}, f_{j}=n^{\frac{5}{2}}$,
$$
	\lim_{ n \to \infty } \frac{n^{2}}{n^{\frac{5}{2}}}
	= \lim_{ n \to \infty } n^{2 - \frac{5}{2}}
	= \lim_{ n \to \infty } n^{-0.5}
	= \lim_{ n \to \infty } \frac{1}{\sqrt{ n }}
	= 0
$$
Therefore, the following holds:
$$
		n^{2} = o\left(n^{\frac{5}{2}}\right)
$$

Thus, $n^{2.5}$ grows asymptotically faster than $n^2$.

### Logarithmic Growth

Using the logarithm power rule, two of the logarithmic functions with exponential inputs can be simplified.

$$
	10\log(n^{3/2}) =10\cdot\frac{3}{2}\log n =15\log n
$$
$$
	\log(n^2)=2\log n
$$

Constant factors do not affect asymptotic growth, so both functions have the same asymptotic growth.
$$
	
2\log n \in \Theta(\log n) \quad\text{and}\quad 15\log n \in \Theta(\log n).
$$

Comparing $\log^{2}{n}$ with $15 \log n$.
$$
	  \lim_{ n \to \infty } \dfrac{\log^{2}n}{15 \log{n}} 
	= \lim_{ n \to \infty }  \dfrac{\log{n}}{15}
	= \infty
$$
This implies $\log^{2}{n} \in \Omega(\log{n})$. More specifically, this implies the following:
$$
	10\log(n^{3/2}) = o(\log^{2}{n})
$$

Therefore, $\log^{2}{n}$ grows asymptotically faster than $10\log(n^{3/2})$ and, by extension, $\log{n^{2}}$.

### Polynomial and Logarithmic

The only remaining comparison is between $\log^{2}{n}$ and $n^2$. Since both functions are squares of positive functions, it suffices to compare $\log n$ and $n$. Let $f_{i} = \log n, f_{j} = n$.

$$
	 \lim_{ n \to \infty } \frac{f_{i}}{f_{j}} 
     = \lim_{ n \to \infty } \dfrac{\log n}{n}
   \overset{\text{L'Hopital}}{=}
     \lim_{ n \to \infty } \frac{\frac{1}{n}}{1} 
     = \lim_{ n \to \infty } \frac{1}{n}
     = 0
$$

Therefore, the following holds:
$$
	\log n = o(n) \quad \log^{2}{n} = o(n^2)
$$

Thus, the final order of the functions based on asymptotic growth (least to greatest) is the following:

- $\log{n^2}$, $10 \log{n^{\frac{3}{2}}}$
- $\log^2{n}$
- $n^2$
- $n^{\frac{5}{2}}$
	
## Code Analysis

Given the following code:
```pseudo
\begin{algorithm} 
\begin{algorithmic} 
	\Procedure{PROCEDURE}{} 
		\State $i \gets n$
		\While{$i > 1$}
			\State $j \gets 0$
			\While{$j < n$}
				\State $j \gets j + 1$
			\EndWhile
			\State $i, j$
			\State $i \gets i / 2$
		\EndWhile
	\EndProcedure 
\end{algorithmic}
\end{algorithm}
```

1. In ters of the input size $n$, how many times will the line $i, j$ be executed? Show your solutions
2. Given your answer in the previous item, provide a tight asymptotic bound for the running time of the code.

## Closed Form

What is the closed form of the following recurrence? Show your solutions

1. $T(n) = T(n - 1) + n$
2. $T(n) = T\left( \dfrac{n}{2} \right) + n$
3. $T(n) = 4 T \left(\dfrac{n}{2}\right) + \lg{n}$
4. $T(n) = 2 T(n - 1) + 2^{n}$
5. $T(n) = T \left( \dfrac{n}{3} \right) + T\left( \dfrac{2n}{3} \right) + \Theta(n)$ 
