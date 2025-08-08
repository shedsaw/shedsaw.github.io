---
title: "Masters Thesis Research"
excerpt: "I discuss my Masters research code results. <br/><img src='/images/masters.png'>"
collection: portfolio
---
The topic of my Master's thesis and research was to analyze and implement a high-order finite volume method for solving the Navier-Stokes equations.
The impetus behind this topic was to study the feasibility of adding such a method to the department's in-house flow solver so that complex flow features
such as vortex shedding could be accurately captured in a computationally efficient manner.

To that end, I reviewed the research literature looking for a suitable algorithm. I focused on the high-order reconstruction method of Dr. Carl Ollivier-Gooch
and his students and collaborators. The method is described as being analogous to ENO and WENO schemes applied to unstructured meshes. To test the method,
I coded up a two-dimensional unstructured solver for the Euler equations, which capture many of the important features of the full Navier-Stokes equations.
Orders of up to fourth are implemented in my research code and are verified using convergence studies with a manufactured solution.

Translating this method a full three-dimensional, parallel unstructured solver was shown to be a challenging endeavor. One reason is that you can get away with
many tricks and still maintain second order accuracy. Numerical integration requires fewer quadrature points. And in a node-centered control volume context, all
partial faces of the control volume must be integrated over to maintain high-order convergence. With a second order scheme, all the partial faces can be agglomerated
into a single face. Another significant issue is that to obtain a low error approximation of the solution's derivatives needed for the reconstruction algorithm,
a reconstruction matrix needs to be constructed with sufficient neighboring control volumes. In a second order scheme, nearest neighboring control volumes is sufficient.
For higher orders, control volumes more than a single edge away need to be considered. This adds cost in a few ways. First, in a parallel setting, more information
needs to be communicated when updating between iterations. A more intensive cost is that the reconstruction matrix problem now needs to be solved with a robust
algorithm such as QR factorization or SVD rather than an existing inexpensive algorithm for second-order reconstruction.

This method may not have been the best fit for the department's flow solver, but the project itself was rewarding. I ingested dozens of research papers and learned much
about a flow solver by coding most everything from scratch. That said, I was not a professional coder and not familiar with good software engineering practices when I wrote
this code. The code is definitely rough but might be helpful for aspiring CFD students.

Links
===
  - [Find the code repository here.](https://github.com/shedsaw/flow-solver)
  - A nice poster that summarizes my thesis abstract and has some nice pictures is [here.](https://www.utc.edu/engineering-and-computer-science/graduate-programs/phd-program/alumni/shane-sawyer)
  - You can find my thesis [here.](https://scholar.utc.edu/theses/74/?_gl=1*ef0ztg*_gcl_au*MTgxMTY2MzU0MC4xNzU0NTk4OTU0)

