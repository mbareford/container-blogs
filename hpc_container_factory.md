A Container Factory for HPC
===========================

This blog post follows on from a previous article entitled [HPC Containers?](hpc_containers.md).

We turn now to the container factory, the environment within which containers are first created and then customised
for various HPC platforms. The container factory is standalone (virtual) machine providing root-level access. 
Specifically, the factory is a Ubuntu 20.04 instance running within the [Eleanor Research Cloud](https://www.ed.ac.uk/information-services/computing/computing-infrastructure/cloud-computing-service/researcher-cloud-service-eleanor) at the [University of Edinburgh](https://www.ed.ac.uk/). It has 8 vCPUs, 16 GB RAM and 160 GB of disk space.

The factory has installed (Sylabs) Singularity 3.8.0.





Initially, the container features an OS (also Ubuntu 20.04) and the GROMACS 2021.1 source code. The container is then
setup as a writable sandbox on ARCHER2 within which GROMACS is built. Following this, the sandbox is converted back to a container image file and
downloaded. The whole "targetting" process is directed from the factory and so can be repeated for other HPC platforms. A final GROMACS container
could therefore hold multiple executables each one targetting a different HPC host (and MPI library).