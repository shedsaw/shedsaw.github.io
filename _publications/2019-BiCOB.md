---
title: "HPC-BLAST: Distributed BLAST for modern HPC clusters."
collection: publications
category: conferences
permalink: /publication/2019-BiCOB
excerpt: 'This paper presents improved results of the HPC-BLAST project.'
date: 2019-03-19
venue: 'BICoB 2019 : 11th International Conference on Bioinformatics and Computational Biology'
bibtexurl: 'https://shedsaw.github.io/files/2019-BiCOB.bib'
citation: 'Shane Sawyer, Mitchel Horton, Chad Burdyshaw, Glenn Brook, and Bhanu Rekapalli. (2019). &quot;HPC-BLAST: distributed BLAST for modern HPC clusters.&quot; <i>Proceedings of 11th International Conference</i>.'
---
The near exponential growth in sequence data available to bioinformaticists, and the emergence of new fields of biological research, continue to fuel an incessant need for increases in sequence alignment performance. Today, more than ever before, bioinformatics researchers have access to a wide variety of HPC architectures including high core count Intel Xeon processors and the many-core Intel Xeon Phi.

In this work, the implementation of a distributed, NCBI compliant, BLAST+ (C++ toolkit) code, targeted for multi- and many-core clusters, such as those containing the Intel Xeon Phi line of products is presented. The solution is robust: distributed BLAST runs can use the CPU only, the Xeon Phi processor or coprocessor, or both by utilizing the CPU or Xeon Phi processor plus a Xeon Phi coprocessor. The distributed BLAST implementation employs static load balancing, fault tolerance, and contention aware I/O. The distributed BLAST implementation, HPC-BLAST, maintains greater than 90% weak scaling efficiency on up to 160 Xeon Phi (Knights Landing) nodes.

The source code and instructions, are available under the Apache License, Version 2.0 at https://github.com/UTennessee-JICS/HPC-BLAST.