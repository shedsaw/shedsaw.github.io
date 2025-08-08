---
title: "Doctoral Research: Spectral fractional Laplacian"
excerpt: "I discuss my PhD research.<br/><img src='/images/extension-rescaled.png'>"
collection: portfolio
---

My doctoral research involved developing a numerical algorithm to efficiently solve the spectral fractional Laplacian. We can dissect this topic starting with the
Laplacian equation itself. Recall that the Laplacian is
\\[ (-\Delta)u = f \,\, , \,\, x \in \Omega \, . \\]
We will restrict ourselves to the case where $$ u=0 \,\, , \,\, x \in \partial \Omega\, $$.
The Laplacian is a second-order elliptic partial differential equation and represents diffusion, or spreading out, of some quantity $$u(x)$$.
The modifier fractional to the Laplacian means that we apply some fraction of the Laplacian operator to that quantity $$u(x)$$ and can be written as
\\[ (-\Delta)^s  = f \,\, , \,\, x \in \Omega \, , \\]
where $$ s \in (0,1) $$.
The fractional Laplacian can be defined in numerous ways. See [this paper](https://arxiv.org/pdf/1507.07356) or
[this paper](https://arxiv.org/pdf/1801.09767) to see some the definitions.

The spectral fractional Laplacian is a particular interpretation. To get a better idea we can briefly discuss spectral theory.
Spectral theory tells us that $$-\Delta$$ has a countable set of eigenpairs $$\{ \lambda_k, \phi_k \}_k$$ such that the $$ \phi_k $$'s
form an orthonormal basis of $$L^2(\Omega)$$. So if we have some smooth function $$w(x)$$, we can expand this function in that basis, i.e.,
\\[ w(x) = \sum_k w_k(x) \phi_k(x) \,\, , \\]
where $$w_k$$ is the Fourier coefficient of $$w(x)$$ with respect to the k-th eigenfunction, $$\phi_k(x)$$. Applying the Laplacian,
\\[ (-\Delta) w(x) = \sum_k w_k (-\Delta)\phi_k(x) = \sum_k w_k \lambda_k \phi_k(x) \,\, . \\]
Now, using this we can define the spectral fractional Laplacian as:
\\[ (-\Delta)^s w(x) = \sum_k w_k (-\Delta)^s \phi_k(x) = \sum_k w_k \lambda_k^s \phi_k(x) \,\, . \\]

The takeaway is that if we know the eigenpairs we can write the solution to the spectral fractional Laplacian directly.
Unfortunately, finding the eigenpairs is both computationally expensive and unstable. Fortunately, Caffarelli and Silvestre showed that the
problem of the spectral fractional Laplacian in $$d$$ dimensions is related to a problem in $$d+1$$ dimensions with no fractional derivatives.
This extended problem is amenable to solving by the finite element method and was extensively studied by doctoral advisor Dr. Abner Salgado
and his collaborators. 

Links
===
  - [Dissertation Defense Slides](https://shedsaw.github.io/files/dissertation-defense-sawyer.pdf)
  - [Access my dissertation here](https://trace.tennessee.edu/utk_graddiss/10419/) - On embargo until 8/15/2025
  - [Submitted Manuscript](https://arxiv.org/pdf/2409.17388)
  - [deal.ii candi Repository](https://github.com/dealii/candi) - Recommended for building deal.ii with libraries on Linux
  - [Source Code Repository](https://github.com/shedsaw/Exact-Diagonalization-Tensor-FEM)