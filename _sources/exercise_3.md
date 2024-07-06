# Exercise 3

```{admonition} Problem 1: Generalization of the concept of phase space in a quantum system
:name: Prob_3-1
:class: tip

The uncertainty principle of quantum mechanics provides a fundamental unit of the phase space volume. Please read the chapter 3.5 of Peliti's textbook about the quantum states and the example to evaluate the occupied phase space by a quantum state using the simple harmonic oscillator. In this problem, we will use another example to check whether we really understand the idea.
Consider a quantum particle of mass $m$ moving in one dimension along a line of length $L$.

1. Show the possible energy values to be $E_n=\frac{\hbar^2\pi^2n^2}{2mL^2}$ where $n=1,2,\dots$.
2. Prove the phase space volume occupied by each quantum state is equal to $h$.
```

```{admonition} Problem 2: *Phase space* : Explain your answer concisely using 3 to 5 sentences.
:name: Prob_3-2
:class: tip

Consider two microscopic states of the same system described by $\xi_{1}(t)$ and $\xi_{2}(t)$. Here, $\xi_i(t)$ is a point in the phase space at time $t$ where $i=1,2$. As time evolves, $\xi_i(t)$ form a path in the phase space. 

1. Can the path $\xi_{1}(t)$ and $\xi_{2}(t)$ intersects with each other under canonical evolution (energy is conserved)?
2. If the energy is not conserved (dissipative force exists), is it possible that the two path ends up at the same point in the phase space? 

Explain why you got this answer or give a simple example to demonstrate your point.
```

```{admonition} Problem 3: Some properties of entropy following Boltzmann's postulate
:name: Prob_3-3
:class: tip

During the lecture, we introduce Boltzmann's postulate

$$
	S=k_B\ln(|\Gamma|)
$$

We want to check whether this new definition fits our understanding of the thermodynamic entropy $S$.

1. Thermodynamic entropy is an extensive quantity: 
	
	1. (Isolated systems): Consider isolated system $A$ and system $B$. The microscopic configurations in the phase space of $A$ and $B$ can be represented by two $\xi_A \in \Gamma_A$ and $\xi_B \in \Gamma_B$ where $\Gamma_A,\Gamma_B$ represent the phase space of the two systems. Since $A$ and $B$ are both isolated, the microscopic configurations of the composite system $A\cup B$ can be described as $\xi^{(A\cup B)}=\{\xi_A,\xi_B\}$. Using this simple setting, calculate the phase space volume of the composite system $A\cup B$ (represent you answers by $\Gamma_A$ and $\Gamma_B$.) and show that the thermodynamic entropy following Boltzmann's definition is an extensive quantity.
	2. (Systems in thermal contact): Consider the two system $A$ and $B$ can exchange energy with each other, but they are isolated from the rest of the world. Therefore, the total energy $E^{(A)}+E^{(B)}=E^{(A|B)}=E$ is kept fixed. Here we use $(A|B)$ to represent the composite system which is the two systems in thermal contact.
	The phase space of the composite system is
	
	$$
		|\Gamma_{(A|B)}|=\sum_{E^{(A)}}|\Gamma^{(A)}(E^{(A)})||\Gamma^{(B)}(E-E^{(A)})|\text{.}
	$$				
	Here, we can assume energy is a continuous variable and approximate the above summation using integral representation, *i.e.*
	
	$$
	|\Gamma_{(A|B)}|\approx \int \frac{dE^{(A)}}{\Delta E^{(A)}} \exp\left[ \frac{1}{k_B}\left( S_{A}(E^{(A)})+S_{B}(E-E^{(A)}) \right) \right]\text{.}
		\label{int_rep}
	$$
	* Convince yourself that this is how things should be when you calculate the phase space of the composite system. After some time, the system reaches equilibrium, so the energy configuration will becomes $E^{(A)}_{eq}+E^{(B)}_{eq}=E$. Notice the fact that the equilibrium configuration will contribute $|\Gamma_{(A|B)_{eq}}|$, which is just one part of the total phase space $|\Gamma_{(A|B)}|$. Expand $E^{(A)}$ in the integral of Eq. (\ref{int_rep}) near the equilibrium configuration $E^{(A)}_{eq}$ up to quadratic order in $(E^{(A)}-E^{(A)}_{eq})$, you will have an expression looks like Gaussian integral. Once you perform the Gaussian integral, you should have
		
		$$	
			|\Gamma_{(A|B)}|\approx |\Gamma_{(A|B)_{eq}}| \times (\text{contribution from the Gaussian integral})\text{.}
		$$
		Identify the system size dependence of the contribution from the Gaussian integral. (Basically, how it depends on $N$ when $N$ is large)
	* In the above derivation, we use $|\Gamma^{(\mu)}(E^{(\mu)})|=\exp\left[ \frac{S_{\mu}(E^{(\mu)})}{k_B} \right]$  with $\mu=A/B$ to express the phase space of individual system initially. After we derive the approximated phase space volume $|\Gamma_{(A|B)}|$, we should be able to evaluate $S_{(A|B)}$ and express it using $S_{A}(E^{(A)}_{eq})$ and $S_{B}(E^{(B)}_{eq})$. Find the difference between $S_{(A|B)}$ and $S^{(A\cup B)}_{eq}\equiv S_{A}(E^{(A)}_{eq})+S_{B}(E^{(B)}_{eq})$. Will this difference be important when $N\to\infty$? If the contribution of this difference is sub-leading in $N$ as $N\to\infty$, we establish the relation that $S_{(A|B)}\approx S^{(A\cup B)}_{eq}= S_{A}(E^{(A)}_{eq})+S_{B}(E^{(B)}_{eq})$.

```

