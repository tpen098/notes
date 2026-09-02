---
aliases: []
tags: []
date created: Wednesday, August 26th 2026, 1:59:16 pm
date modified: Thursday, August 27th 2026, 10:30:02 pm
---

# CS 197 WZZQ - Assessment 03

Submitted by Stephen Singer (2019-05493) on August 27, 2026.

## Asymptotic Growth Rate Analysis

Consider the following functions, organized by asymptotic growth rate:

* $n^{5/2}$
* $\log(n^2)$
* $n^2$
* $10 \log(n^{3/2})$
* $\log^2 n$

Given two algorithms for the same problem with time complexities $O(f_i(n))$ and $O(f_j(n))$, the relative growth is defined by the following limit:

$$
\lim_{n \to \infty} \frac{f_i(n)}{f_j(n)} = \begin{cases} 
    0 & \implies f_i(n) = O(f_j(n)) \quad (\text{slower growth}) \\
    c \in (0, \infty) & \implies f_i(n) = \Theta(f_j(n)) \quad (\text{same growth rate}) \\
    \infty & \implies f_i(n) = \Omega(f_j(n)) \quad (\text{faster growth}) 
\end{cases}
$$

There are $\binom{5}{2} = 10$ unique pairs of functions $(f_i, f_j)$ to compare. However, the analysis can be simplified by grouping functions with the same asymptotic behavior.

### Logarithmic Growth

Using the logarithm power rule, the first two logarithmic functions simplify to the following:

$$
\begin{aligned}
    \log(n^2) &= 2 \log n \in \Theta(\log n) \\
    10 \log(n^{3/2}) &= 10 \cdot \frac{3}{2} \log n = 15 \log n \in \Theta(\log n)
\end{aligned}
$$

Let $f_i(n) = \log(n^2)$ and $f_j(n) = 10 \log(n^{3/2})$. Evaluating their ratio shows that scaling does not affect asymptotic growth:

$$
\lim_{n \to \infty} \frac{\log(n^2)}{10 \log(n^{3/2})} = \lim_{n \to \infty} \frac{2 \log n}{15 \log n} = \frac{2}{15} \implies \log(n^2) = \Theta(10 \log(n^{3/2}))
$$

Now, let $f_i(n) = 10 \log(n^{3/2})$ and $f_j(n) = \log^2 n$. Evaluating their ratio shows that $\log^2 n$ grows faster:

$$
\lim_{n \to \infty} \frac{15 \log n}{\log^2 n} = \lim_{n \to \infty} \frac{15}{\log n} = 0 \implies 10 \log(n^{3/2}) = O(\log^2 n)
$$

### Polynomial and Logarithmic Growth

Consider $f_i(n) = \log n$ and $f_j(n) = n$. Using L'Hopital's Rule shows that $n$ grows faster than $\log n$:

$$
\lim_{n \to \infty} \frac{\log n}{n} \overset{\text{L'H}}{=} \lim_{n \to \infty} \frac{1/n}{1} = 0 \implies \log n = o(n)
$$

Squaring both functions for $f_i(n) = \log^2 n$ and $f_j(n) = n^2$, the same conclusion applies:

$$
\lim_{n \to \infty} \frac{\log^2 n}{n^2} = 0 \implies \log^2 n = o(n^2)
$$

### Polynomial Growth

Let $f_i(n) = n^2$ and $f_j(n) = n^{5/2}$. Evaluating their ratio shows that $n^{5/2}$ grows faster than $n^2$:

$$
\lim_{n \to \infty} \frac{n^2}{n^{5/2}} = \lim_{n \to \infty} n^{2 - 5/2} = \lim_{n \to \infty} \frac{1}{\sqrt{n}} = 0 \implies n^2 = O\left(n^{5/2}\right)
$$

### Conclusion

The final order of the functions based on asymptotic growth (from least to greatest) is:

1. $\log(n^2),\, 10 \log(n^{3/2})$
2. $\log^2 n$
3. $n^2$
4. $n^{5/2}$

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
				\State $i, j$
				\State $j \gets j + 1$
			\EndWhile
			\State $i \gets i / 2$
		\EndWhile
	\EndProcedure 
\end{algorithmic}
\end{algorithm}
```

### Integer Division Approach

The procedure will continue to print $i$ with every number $j \in [0, n-1]$ or $n$ times. However, $i$ is repeatedly halved and will halt the problem once it reaches 1. Let $c$ be the number of times $i$ can be halved before it becomes 1. Then the number of times $i, j$ will be executed is $nc$ times.

Let's assume $n$ is an integer and division will lead to the floor of the division (integer division). Consider initial cases of $n$:

$$
	\begin{align}
	n=1:& c=0 & 1 \\
	n=2:& c=1 & (2 \to 1) \\
	n=3:& c=1 & (3 \to 1) \\
	n=4:& c=2 & (4 \to 2 \to 1)\\
	n=5:& c=2 & (5 \to 2 \to 1)\\
	n=6:& c=2 & (6 \to 3 \to 1)\\
	n=7:& c=2 & (7 \to 3 \to 1)\\
	n=8:& c=3 & (8 \to 4 \to 2 \to 1)\\
	\end{align}
$$

Notice that on powers of $2$, $c$ increases by one. Given a base of $2$, $c$ can be determined by what power would be needed to make it reach the value of $n$. In other words, $c$ is logarithmic. However, it's not exactly $c=\lg{n}$. Consider the first values of $\lg{n}$:

$$
\begin{align} 
\lg 1 &= 0 \\
\lg 2 &= 1 \\
\lg 3 &\approx 1.5850 \\
\lg 4 &= 2 \\
\lg 5 &\approx 2.3219 \\
\lg 6 &\approx 2.5850 \\
\lg 7 &\approx 2.8074 \\
\lg 8 &= 3 \\
\end{align}
$$

The pattern matches when $c = \lfloor \lg n  \rfloor$. Therefore, the line $i, j$ will run $n \lfloor \lg{n} \rfloor$ times on integer division implementation.

### Normal Division Approach

If normal division is used, the formula alters slightly:

$$
	\begin{align}
	n=1:& c=0 & 1 \\
	n=2:& c=1 & (2 \to 1) \\
	n=3:& c=2 & (3 \to 1.5 \to 0.75) \\
	n=4:& c=2 & (4 \to 2 \to 1)\\
	n=5:& c=3 & (5 \to 2.5 \to 1.25 \to 0.625)\\
	n=6:& c=3 & (6 \to 3 \to 1.5 \to 0.75)\\
	n=7:& c=3 & (7 \to 3.5 \to 1.75 \to 0.875)\\
	n=8:& c=3 & (8 \to 4 \to 2 \to 1)\\
	\end{align}
$$

The pattern matches when $c=\lceil \lg{n} \rceil$ instead. Therefore, the line $i, j$ will run $n\lceil \lg{n} \rceil$ times on normal division implementation.

### Tight Asymptotic Bound

#### Floor Function Definition

Given the nature of the running time, let's compare it with running time $n \lg{n}$
Consider $f_{i}=n \lfloor \lg{n} \rfloor$, $f_{j}=n \lg{n}$.

$$
	\lim_{ n \to \infty } \dfrac{n \lfloor \lg{n} \rfloor}{n \lg{n}} 
	= \lim_{ n \to \infty }  \dfrac{\lfloor \lg{n} \rfloor}{\lg{n}}
$$

Note that the floor function bounds a value $x$ between $x-1$ and $x$

$$
	x - 1 \lt \lfloor x \rfloor  \le x
$$

With $x=\lg{n}$:

$$
		\lg{n} - 1 \lt \lfloor \lg{n} \rfloor \le \lg{n}
$$

Dividing by $\lg{n}$:

$$
			\frac{\lg{n} - 1}{\lg{n}} \lt \frac{\lfloor \lg{n} \rfloor}{\lg{n}} \le 1
$$

$$
			1-\frac{1}{\lg{n}} \lt \frac{\lfloor \lg{n} \rfloor}{\lg{n}} \le 1
$$

Using the squeeze theorem, if both sides of the inequality approach the same limit, then the middle term should approach the same limit.

Since the right side is a constant, it's a given that it will approach a constant, specifically $1$:

$$
\lim_{ n \to \infty } 1 = 1	
$$

On evaluation, the left side also approaches $1$

$$
	\lim_{ n \to \infty } 1-\frac{1}{\lg{n}} = 1  - 0= 1
$$

Therefore,

$$
	\lim_{ n \to \infty }  \dfrac{\lfloor \lg{n} \rfloor}{\lg{n}} = 1
$$

Given it's a constant, then it can be concluded that with the floor function definition, the following holds:

$$
	n \lfloor \lg{n} \rfloor \in \Theta(n \lg{n})
$$

#### Ceiling Function Definition

Given the nature of the running time, let's compare it with running time $n \lg{n}$ again.
Consider $f_{i}=n \lceil \lg{n} \rceil$, $f_{j}=n \lg{n}$.

$$
	\lim_{ n \to \infty } \dfrac{n \lceil \lg{n} \rceil}{n \lg{n}} 
	= \lim_{ n \to \infty }  \dfrac{\lceil \lg{n} \rceil}{\lg{n}}
$$

The ceiling function bounds the value in the following manner:

$$x \le \lceil x \rceil \lt x + 1$$

With $x=\lg{n}$:

$$
		\lg{n} \le \lceil \lg{n} \rceil \lt \lg{n} + 1
$$

Dividing by $\lg{n}$:

$$
			1 \le \frac{\lceil \lg{n} \rceil}{\lg{n}} \lt \frac{\lg{n} + 1}{\lg{n}}
$$

$$
			1 \le \frac{\lceil \lg{n} \rceil}{\lg{n}} \lt \frac{1}{\lg{n}} +1
$$

The limit of the right side approaches $1$ still.

$$
	\lim_{ n \to \infty } \frac{1}{\lg{n}} +1 = 0 + 1 = 1
$$

Using the sandwich theorem again, it can be concluded that the expression has a constant limit

$$
	\lim_{ n \to \infty }  \dfrac{\lceil \lg{n} \rceil}{\lg{n}} = 1
$$

Given it's also a constant, the following holds:

$$
	n \lceil \lg{n} \rceil \in \Theta(n \lg{n})
$$

# Closed Form

## First Function

The first given recursive function can be rewritten as the following:

$$
	\begin{align}
	 T(n) 
	    &= T(n-1) + n  \\
		&= T(n-1) + (n - 0) \\
	\end{align}
$$

With this definition, $T(n-1)$ and $T(n-2)$ can be derived:

$$
	\begin{align}
	T(n-1) &= T((n-1) - 1) + (n - 1) &= T(n-2) + (n - 1) \\
	T(n-2) &= T((n-2) - 1) + (n - 2) &= T(n-3) + (n - 2)
	\end{align}
$$

Substituting $T(n-1)$ directly, the same function can be interpreted as the following:

$$
	\begin{align}
	 T(n) 
		&= [T((n-1) - 1) + (n-1)] + n  \\
		&= T(n - 2) + (n - 1) + (n - 0) \\ 
	\end{align}
$$

Applying the same concept, substituting $T(n-2)$, the function can be interpreted as the following:

$$
	\begin{align}
     T(n)
	    &= [T((n-2) - 1) + (n-2)] + (n - 1) + n  \\
		&= T(n - 3) + (n - 2) + (n - 1) + (n - 0) \\
	\end{align}
$$

From the following steps up to the $i$-th step, the function takes the following form:

$$
T(n) = T(n-i) + \sum_{k=0}^{i-1} (n - k)
$$

The summation can be simplified further as shown:

$$
\begin{align}
 \sum_{k=0}^{i-1} (n - k) 
 &= \sum_{k=0}^{i-1} n - \sum_{k=0}^{i-1} k \\
 &= in - \dfrac{i(i-1)}{2} \\
 &= \dfrac{2in - i^{2} + i}{2}
\end{align}
 $$

Substituting back, the function takes the following form:

$$T(n) = T(n-i) + \dfrac{2in - i^2 + i}{2}$$

The function should work for any value of $i$. Using this knowledge, if $i = n$, then $T(0)$ is reached and a closed looped form is achieved.

$$
	\begin{align}
	T(n)  
	&= T(0) + \dfrac{2n^{2}-n^{2}+n}{2}  \\
	&= T(0) + \dfrac{n^{2}+n}{2}
	\end{align}
$$

Looking at the function, the largest term is within the form of $n^{2}$. Assuming $T(0) = c \in \mathbb{R}$, let $f_{i} = \frac{n^{2} + n}{2}$, $f_{j} = n^{2}$. Then, the asymptotic growth of $T(n)$ can be determined with respect to $n^{2}$.

$$
	\lim_{ n \to \infty }  \frac{\frac{n^{2} + n}{2}}{n^{2}}
	=\lim_{ n \to \infty }  \frac{1}{2} + \lim_{ n \to \infty }\frac{1}{2n}
	= \frac{1}{2} + 0
$$

Therefore, $T(n) = \Theta(n^{2})$

## Second Function

The second given recursive function can be rewritten as the following:

$$
	\begin{align}
	 T(n) 
	    &= T\left( \frac{n}{2} \right) + n  \\
		&= T\left( \frac{n}{2^{1}} \right) + \frac{n}{2^{0}} 
	\end{align}
$$

With this definition, $T\left( \frac{n}{2^{1}} \right)$ and $T\left( \frac{n}{2^{2}} \right)$ can be derived:

$$
	\begin{align}
	 T\left( \frac{n}{2^{1}} \right) 
	    &= T\left( \frac{\frac{n}{2}}{2} \right) + \frac{n}{2}
		&=  T\left( \frac{n}{2^{2}} \right) + \frac{n}{2} \\
	 T\left( \frac{n}{2^{2}} \right)
	    &= T\left( \frac{\frac{n}{2^{2}}}{2} \right) + \frac{n}{2^{2}}
		&=  T\left( \frac{n}{2^{3}} \right) + \frac{n}{2^{2}} \\
	\end{align}
$$

Substituting $T\left( \frac{n}{2} \right)$ directly, the same function can be interpreted as the following:

$$
	\begin{align}
	 T(n) 
	    &= \left\{ T\left( \frac{\left[\frac{n}{2}\right]}{2} \right) + \frac{n}{2} \right\} + n  \\
		&= T\left( \frac{n}{2^{2}} \right) + \frac{n}{2^{1}} + \frac{n}{2^{0}} 
	\end{align}
$$

Applying the same concept, substituting $T\left( \frac{n}{2^{2}} \right)$, the function can be interpreted as the following:

$$
	\begin{align}
	 T(n) 
	    &= \left\{ T\left( \frac{\left[\frac{n}{2^{2}}\right]}{2} \right) + \frac{n}{2^{2}} \right\} + \frac{n}{2} + n  \\
		&= T\left( \frac{n}{2^{3}} \right) + \frac{n}{2^{2}} + \frac{n}{2^{1}} + \frac{n}{2^{0}} 
	\end{align}
$$

From the following steps up to the $i$-th step, the function takes the following form:

$$
	T(n) = T\left( \frac{n}{2^{i}} \right) + \sum_{k=0}^{i-1} \frac{n}{2^{k}}
$$

The summation can be simplified further as shown:

$$
\begin{align}
 \sum_{k=0}^{i-1} \frac{n}{2^{k}}
 &= n \cdot \sum_{k=0}^{i-1} \left(\frac{1}{2}\right)^{k} \\
 &= n \cdot \dfrac{1 - \left( \frac{1}{2} \right)^{i}}{1 - \frac{1}{2}} \\
 &= n \cdot \dfrac{1 - \left( \frac{1}{2} \right)^{i}}{\frac{1}{2}} \\
 &= n \cdot 2 \cdot \left( 1 - \left(\frac{1}{2}\right)^{i} \right) \\
 &= 2n \left( 1 - \frac{1}{2^{i}} \right)
\end{align}
$$

Substituting back, the function takes the following form:

$$
	T(n) 
      = T\left( \frac{n}{2^{i}} \right)
      +  2n \left(  1 - \frac{1}{2^{i}} \right)
$$

The function should work for any value of $i$. Using this knowledge, if $i = \log_{2}{n}$, then $T(1)$ is reached and a closed looped form is achieved.

$$
	\begin{align}
	T(n)  
	&= T(1) + 2 n \left(  1 - \frac{1}{2^{\log_{2}{n}}} \right)  \\
	&= T(1) + 2 n \left(  1 - \frac{1}{n} \right)  \\
	&= T(1) + 2 n - 2  \\
	\end{align}
$$

Looking at the function, the largest term is within the form of $n$. Assuming $T(1) = c \in \mathbb{R}$, let $f_{i} = 2 n - 2$, $f_{j} = n$. Then, the asymptotic growth of $T(n)$ can be determined with respect to $n$.

$$
	\lim_{ n \to \infty }  \frac{2n - 2}{n} 
	= \lim_{ n \to \infty }  2 - \lim_{ n \to \infty } \frac{2}{n}
	= 2 - 0
$$

Therefore, $T(n) = \Theta(n)$

### Third Function

The third recursive function can be rewritten in the following form for convenience.

$$
		T(n) = 4 T \left(\dfrac{n}{2}\right) + \lg{\frac{n}{2^{0}}} \\
$$

Solving for $T\left( \frac{n}{2} \right)$, $T(n)$ can be given an alternate form via substitution:

$$
	\begin{align}
	T\left( \frac{n}{2} \right)
	     &= 4 T \left(\dfrac{n}{2^{2}}\right) + \lg{\frac{n}{2}} \\
	T(n)
		 &= 4 \left[ 4 T\left(\frac{n}{2^{2}}\right) + \lg\left(\frac{n}{2}\right) \right] + \lg n  \\
	     &=  4^2 T\left(\frac{n}{2^2}\right) + 4\lg\left(\frac{n}{2}\right) + \lg \frac{n}{2^{0}}
	\end{align}
$$

The same principle applies for $T\left( \frac{n}{2^{2}} \right)$, $T(n)$ can be given an alternate form via substitution:

$$
	\begin{align}
	T\left( \frac{n}{2^{2}} \right)
	     &= 4 T \left(\dfrac{n}{2^{3}}\right) + \lg{\frac{n}{2^{2}}} \\
	T(n)
		 &= 4^{2} \left[ 4 T\left(\frac{n}{2^{3}}\right) + \lg{\frac{n}{2^{2}}} \right] + 4\lg{\frac{n}{2^{1}}}+ \lg \frac{n}{2^{0}}  \\
	     &=  4^3 T\left(\frac{n}{2^3}\right) + 4^{2}\lg{\frac{n}{2^{2}}} + 4\lg{\frac{n}{2^{1}}}+ \lg \frac{n}{2^{0}}
	\end{align}
$$

From the following steps up to the $i$-th step, the function takes the following form:

$$
	T(n) = 4^{i} T\left( \frac{n}{2^{i}} \right) + \sum_{k=0}^{i-1} 4^{k}\lg{\frac{n}{2^{k}}}
$$

The summation can be simplified further as shown:

$$
\begin{align}
  \sum_{k=0}^{i-1} 4^{k}\lg{\frac{n}{2^{k}}}
  &= \sum_{k=0}^{i-1} 4^{k} \lg{n} - \sum_{k=0}^{i-1} 4^{k} \lg{2^k} \\
  &= \lg{n} \sum_{k=0}^{i-1} 4^{k} - \sum_{k=0}^{i-1} k \cdot 4^{k} \\
  &= \lg{n} \dfrac{4^{i} - 1}{4 - 1} - \sum_{k=0}^{i-1} k \cdot 4^{k}
\end{align}
$$

The right side needs some series manipulation to further simplify:

$$
\begin{align}
 S 
 &= \sum_{k=0}^{i-1} k \cdot 4^{k} \\
 &= 0 \cdot 4^{0} + 1\cdot 4^{1} + 2 \cdot 4^{2} + \dots + (i - 1) \cdot 4^{i - 1}  \\
 4S
 &= 0 \cdot 4^{1} + 1\cdot 4^{2} + 2 \cdot 4^{3}  + \dots  + (i-1) \cdot 4^{i} \\
 S-4S 
 &= 0 \cdot 4^{0} + 1\cdot 4^{1} + 2 \cdot 4^{2}  + \dots + (i - 1) \cdot 4^{i - 1} \\
 &\quad\quad\quad\quad - 0 \cdot 4^{1} - 1\cdot 4^{2} - \dots - (i-2) \cdot 4^{i - 1} - (i-1) \cdot 4^{i} \\
 &= 4^{1} + 4^{2} + 4^{3} + \dots +  4^{i-1} - (i - 1) \cdot 4^{i } \\ 
  &= \bbox[cyan, 4px]{4^{0}} + 4^{1} + 4^{2} + 4^{3} + \dots +  4^{i-1} - (i - 1) \cdot 4^{i } \bbox[cyan, 4px]{-4^{0}} \\
 -3S  
 &= \sum_{k=0}^{i-1} 4^{k} - (i - 1) \cdot 4^{i} - 1\\
 &= \dfrac{4^{i} - 1}{4 - 1} - (i - 1) \cdot 4^{i} - 1\\
 &= \dfrac{4^{i} - 1 - 3i \cdot 4^{i} + 3 \cdot 4^{i} - 3}{3} \\
 &= \dfrac{4^{i}(4 - 3i) - 4}{3} \\
 S
 &= \dfrac{4^{i}(3i - 4) + 4}{9}
\end{align}
$$

Substituting back, the function $T(n)$ takes the following form:

$$
	T(n) 
	= 4^{i} T\left( \frac{n}{2^{i}} \right) 
	+ \lg{n} \dfrac{4^{i} - 1}{4 - 1}
	- \dfrac{4^{i}(3i - 4) + 4}{9}
$$

The function should work for any value of $i$. Using this knowledge, if $i = \lg{n}$, then $T(1)$ is reached and a closed looped form is achieved.

$$
\begin{align}
	T(n) 
	&= 4^{\lg{n}} T\left( 1 \right) 
	+ \lg{n} \dfrac{4^{\lg{n}} - 1}{4 - 1}
	- \dfrac{4^{\lg{n}}(3\lg{n} - 4) + 4}{9} \\
\end{align}
$$

Given the following simplification:

$$
	4^{\lg{n}} = (2^{2})^{\lg{n}} = (2^{\lg{n}})^{2} = n^{2}
$$

The closed form of the function can be further reduced to the following form:

$$
	\begin{align}
	T(n) 
	&= n^{2} T\left( 1 \right) 
	+ \lg{n} \dfrac{n^{2} - 1}{3}
	- \dfrac{n^{2}(3\lg{n} - 4) + 4}{9} \\ 
	&= n^{2} T\left( 1 \right) 
	+ \dfrac{3n^{2} \lg{n}  - 3 \lg{n}}{9}
	- \dfrac{n^{2}(3\lg{n} - 4) + 4}{9}  \\
	&= n^{2} T\left( 1 \right) 
	+ \dfrac{4n^{2} - 3 \lg{n} - 4}{9}
	\end{align}
$$

Looking at the function, the largest term is within the form $n^{2}$. Assuming $T(1) = c \in \mathbb{R}$, let $f_{i} = n^{2}c + \frac{4}{9}n^{2} - \frac{3\lg{n}}{9} - \frac{4}{9}$ and $f_{j} = n^{2}$. Then, the asymptotic growth of $T(n)$ can be determined with respect to $n^{2}$.

$$
	\begin{align}
	\lim_{ n \to \infty } \frac{n^{2}c + \frac{4}{9}n^{2} - \frac{3\lg{n}}{9} - \frac{4}{9}}{n^{2}}
	&= \lim_{ n \to \infty } c + \lim_{ n \to \infty } \frac{4}{9} - \lim_{ n \to \infty }\frac{3\lg{n}}{9n^{2}} - \lim_{ n \to \infty }\frac{4}{9n^{2}} \\
	&= \frac{9c - 4}{9} - \lim_{ n \to \infty } \frac{3\lg{n}}{9 n^{2}} - 0 \\
	&= \frac{9c - 4}{9}
	\end{align}
$$

Therefore, $T(n) = \Theta(n^{2})$

### Fourth Function

The first function does not need preparation. Note the process will be similar to the first function.

 $$
	T(n) = 2 T(n - 1) + 2^{n}
 $$

Based on the function definition, $T(n-1)$ and $T(n-2)$ can be derived:

$$
	\begin{align}
	T(n-1) 
	&= 2T((n-1)-1) + 2^{n-1} 
	&= 2 T(n-2) + 2^{n-1} \\
	T(n-2) 
	&= 2T((n-2)-1) + 2^{n-2} 
	&= 2 T(n-3) + 2^{n-2}
	\end{align}
$$

Substituting $T(n-1)$ directly to $T(n)$, the function takes the following form:

$$
	T(n) = 2 [2 T(n-2) + 2^{n-1}] + 2^{n} = 2^{2} T(n-2)+ 2^{n} + 2^{n}
$$

Substituting $T(n-2)$ directly to $T(n)$, the function takes the following form:

$$
	T(n) = 2^{2} [2 T(n-3) + 2^{n-2}] + 2^{n} + 2^{n} = 2^{3} T(n-3)+ 2^{n} + 2^{n} + 2^{n}
$$

From the following steps up to the $i$-th step, the function takes the following form:

$$
	T(n) = 2^{i} T(n-i) + 2^{n} i
$$

The function should work for any value of $i$. Using this knowledge, if $i = n$, then $T(0)$ is reached and a closed looped form is achieved.

$$
	T(n) = 2^{n} T(0) + 2^{n} n = 2^{n} (T(0) + n)
$$

Looking at the function, the largest term is within the form of $n2^{n}$. Assuming $T(0) = c \in \mathbb{R}$, let $f_{i} = c2^{n} + n2^{n}$, $f_{j} = n2^{n}$. Then, the asymptotic growth of $T(n)$ can be determined with respect to $n2^{2}$.

$$
	\lim_{ n \to \infty } \frac{c2^{n} + n2^{n}}{n2^{n}} \\
	= \lim_{ n \to \infty } \frac{c}{n} + \lim_{ n \to \infty } 1
	= 0 + 1
$$

Therefore, $T(n) = \Theta(n2^{2})$

### Fifth Function

 $T(n) = T \left( \dfrac{n}{3} \right) + T\left( \dfrac{2n}{3} \right) + \Theta(n)$

![[Pasted image 20260827204129.png]]
