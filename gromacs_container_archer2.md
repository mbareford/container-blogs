GROMACS in a Container on ARCHER2
=================================

Containers are a convenient means of encapsulating complex software environments, but can this convenience be realised for parallel research codes?

Running such codes costs money, which means that code performance is often tuned to specific supercomputer platforms. Therefore, for containers to
be useful in the world of HPC, it must be possible to capture this specialisation within a single container. Indeed a container should be dedicated
to one research code and have the ability to run efficiently on multiple HPC platforms.

In this way, containers could facilitate reproducibility and portability by allowing scientists to concentrate on the results of their simulations
rather than on the sometimes fiddly compilation scripts necessary for good performance.

Is this a realistic expectation?

Creating a containerized code such that it can run indistinguishably from its non-containerized form is likely to be a painstaking process, sensitive
to the choice of code, compiler, MPI library and HPC host.  I attempt therefore to answer this question on a case-by-case basis.

We start with a containerized GROMACS code running on ARCHER2.

![GROMACS Results](./images/gromacs-ssp-simtime.eps)