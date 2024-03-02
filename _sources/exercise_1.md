# Exercise 1

* Some Gaussian integrals:
	1. Evaluate the simple generalization of the Gaussian integral we discussed in the lecture.
	   
		$$	
			\int_{-\infty}^{\infty}e^{-ax^2+bx}dx=?
		$$
		
	2. A $N$ dimensional Gaussian integral is defined as
	   
	   $$
			\int_{-\infty}^{\infty}dx_1
			\int_{-\infty}^{\infty}dx_2
			\cdots
			\int_{-\infty}^{\infty}dx_N
			\exp\left[ -\frac{1}{2}\sum_{i,j=1}^{N} x_i A_{ij} x_j+\sum_{i=1}^{N} b_ix_i \right]
	   $$
		Derive the final expression of this integral using the matrix $A$ and the vector $b$. Here we assume the matrix $A$ is diagonalizable with positive eigenvalues.
	3. Fourier transform for Gaussian--
	   
	   $$
			G(x,t)=\frac{1}{2\pi}\int_{-\infty}^{\infty}e^{ikx}e^{-Dk^2t}dk
	$$
		Evaluate this integral by complete the square of the exponent and change the complex integration contour correspondingly.
		One should find the result that $G(x,t)=\frac{1}{\sqrt{4\pi Dt}}e^{-x^2/(4Dt)}$.

