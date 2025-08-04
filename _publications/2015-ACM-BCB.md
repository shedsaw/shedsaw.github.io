---
title: 'HPC-BLAST: distributed BLAST for xeon phi clusters'
collection: publications
category: posters
permalink: /publication/2015-ACM-BCB
excerpt: 'A poster presentation for early HPC-BLAST architecture.'
date: 2015-09-12
venue: '6th ACM Conference on Bioinformatics, Computational Biology and Health Informatics'
paperurl: 'http://shedsaw.github.io/files/hpc_blast_poster_two_logos10.pdf'
---
he near exponential growth in sequence data available to bioinformaticists, and the emergence of new fields of biological research, continue to fuel an incessant need for increases in sequence alignment performance. Concurrently, the High Performance Computing (HPC) world has seen a steady increase in the use of the Intel Xeon Phi. This is depicted by the concentration of TOP500 machines that use Phi accelerators, from November 2012 to November 2014, in six month intervals: 0.40%, 1.60%, 1.80%, 2.80%, and 3.4%. Today, more than ever before, bioinformatics researchers have access to a wide variety of HPC architectures.
To the best of our knowledge, we are the first to implement a distributed, NCBI compliant, BLAST+ (C++ toolkit) code, for Intel Xeon Phi clusters. Our solution is robust: distribted BLAST runs can use the CPU only, the Phi only, or both (symmetric mode). We employ dynamic load balancing, fault tolerance, and contention avoiding I/O. Our distributed BLAST implementation, HPC-BLAST, maintains 90% weak scaling efficiency to 128 Xeon Phis.
