# Research

Below, you can find a description of several areas of research the SCOPA lab has contributed to. Code related to our research is deployed at [https://github.com/scopagroup](https://github.com/scopagroup).


## Diffeomorphic Image Registration

We have developed the software tool CLAIRE for diffeomorphic image registration in 3D. CLAIRE stands for <em>Constrained Large Deformation Diffeomorphic Image Registration</em>. It is a C/C++ software package for velocity-based diffeomorphic image registration. It is based on a PDE-constrained variational problem formulation. The governing PDEs are transport equations. Its performance is optimized for multi-core CPU systems (cpu branch) and multi-node, multi-GPU architectures (gpu branch; default). The CPU version uses MPI for data parallelism, and has been demonstrated to scale on several supercomputing platforms. CLAIRE can be executed on large-scale state-of-the-art computing systems as well as on local compute systems with limited resources.

CLAIRE has been released under the GNU General Public License and is avaialbe for download at [https://github.com/andreasmang/claire](https://github.com/andreasmang/claire). The deployment page is [https://andreasmang.github.io/claire](https://andreasmang.github.io/claire).


## Diffeomorphic Shape Matching and Shape Analysis

We have developed numerical algorithms for studying the variability of shapes and shape deformations though the lens of geodesic flows of diffeomoprhisms. We formulate diffeomorphic shape matching as n ODE-constrained optimization problem. The ODDE constraint models the flow of diffeomorphisms.




## Support
* since 2022: NSF CAREER Award (Computational Mathematics) ([DMS-2145845](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2145845))
* 2020--2023: NSF Applied Mathematics ([DMS-2009923](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2009923))
* 2020--2023: NSF Computational Mathematics ([DMS-2012825](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2012825))
* 2019--2022: NSF CDS&E-MSS ([DMS-1854853](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1854853))
* 2019: NVIDIA Corporation GPU Grant Program (Accelerated Data Science Call)
* 2018: SIMONS Foundation Collaboration Grants for Mathematicians (Award 586055)
