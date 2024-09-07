### Enhanced Sampling of Biomolecular Slow Conformational Transitions Using Adaptive Sampling and Machine Learning

Mingyuan Zhang, Hao Wu, Yong Wang

This is the official implementation of the algorithm proposed in the paper "Enhanced Sampling of Biomolecular Slow Conformational Transitions Using Adaptive Sampling and Machine Learning". Due to the Github file size/number restraint, we only upload the python scripts for the implementation and post-simulation analysis here. For the complete simulation/analysis files that is able to replicate all the results/figures in the paper, please refer to this Zenodo entry: https://zenodo.org/records/13294161.

There are two directories, `ala2/` and `ala10/` under the main directory, corresponding to the two examples demonstrated in this study. The file structure under these directories are similar, consisting of:

- `ala2.ipynb` or `ala10.ipynb`: the implementation of the automated pipeline. This automated pipeline used PLUMED patched Gromacs (both standard and the mpi version) for both adaptive sampling and OPES simulations. PLUMED is also used to generate featurized trajectory dataset as `COLVAR` files. Several widely used packages are used for MSM construction and seed `.gro` files generation. We implemented the count-based seed selection strategy inside the script on our own so that one can perform count-based adaptive sampling with Gromacs. Notice that this script can be slightly modified to perform adaptive sampling only. For such implementation, see the modified `.ipynb` file in the Zenodo entry.
- `AdaptiveSamplingAnalysis.ipynb`: the analysis script for adaptive sampling trajectories.
- `compare_with_msm.ipynb`: the analysis script for the comparison of the proposed algorithm to the commonly used adaptive sampling+MSM approach.
- `opes/COLVAR/analysis.ipynb`: the analysis script for OPES trajectories.

Notice that running `ala2.ipynb` or `ala10.ipynb` has a strict requirement of the directory structure. One can modify such structure by directly altering these scripts. An easier way to use this script is to follow the directory structure in the Zenodo entry. For any question, feel free to raise an issue or email mingyuanzhang@zju.edu.cn.