# tauRAMD
**A collection of Python scripts for computations of relative protein-ligand residence times using tauRAMD (Random Acceleration Molecular Dynamics)**

Author: Daria Kokh

Heidelberg Institute of Theoretical Studies (HITS, www.h-its.org)

Schloss-Wolfsbrunnenweg 35

69118 Heidelberg, Germany

_This open source software code was developed in part in the Human Brain Project, funded from the European Union’s Horizon 2020  Framework Programme for Research and Innovation under Specific Grant Agreements  No. 785907 (Human Brain Project  SGA2)._


### This repository has been moved and will be mantained at https://github.com/HITS-MCM/tauRAMD.  Please use this link  for the updates


## Ligand_swap_out
A set of scripts that helps to swap out ligands in a protein-ligand complex

## tauRAMD-v2.py
 
Script for computation of drug-target relative residence times from Random Acceleration Molecular Dynamics (RAMD)simulations.
It also provides statistical analysis of the results. 
    
    PREREQUISITE
    1. Multiple (at least 10) RAMD dossociation trajectories must be generated using either Gromacs or NAMD software
    In the later case script must be modified a bit:  
    soft = "Gr" must be changed to 
    soft = "NAMD"
    2. lines of the output files where ligand dissociation is reported
    for Gromacs: “XX/YYYY.out:==== RAMD ==== GROMACS will be stopped after xxxxx steps.”
    for NAMD: "EXIT: xxxxx  > LIGAND EXIT EVENT DETECTED: STOP SIMULATION"
    must ge collected in a single file or in multiple files (if trajectories were started from different input coordinate and velocities files) 
    USAGE
    tauRAMD-v1.py  input_file[s]
    input files must contain a set of lines extracted from the gromacs output. Each line contains the number of steps executed before dissociation 
    and has the following format: “XX/YYYY.out:==== RAMD ==== GROMACS will be stopped after 874650 steps.”
    or if RAMD simulations were done using NAMD software: "EXIT: 462950  > LIGAND EXIT EVENT DETECTED: STOP SIMULATION"
    OUTPUT
    residence time with the standard deviation computed for each input_file and an images with representation of the bootstrapping output and statistics
    ''')
    

