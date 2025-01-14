![image](image_distortion.png)

[![DOI](https://zenodo.org/badge/392753173.svg)](https://zenodo.org/badge/latestdoi/392753173)
# Overview
Polyhedron distortion analysis using group theory.
This could either be used as a standalone script or as an API.

# Background
This code allows you to convert distortions into a small-sized vector, possibly suitable for machine learning input.
Example for octahedron is given, but it is applicable to any type of polyhedron.

# Contents
## Dependencies
- numpy
- phonopy (developed with version 2.8)
- pymatgen (developed with version 2022.0.8)

## Installation
The two scripts `basis_generator.py` and `polyhedron_analysis.py` does not rely on each other.
Installation procedure is same as other python scripts.

If you want to use it as a script, you can simply execute it anywhere.

If you want to use the API, you could either:
- export PYTHONPATH=\<full path to the polyhedron_distortion directory\>:$PYTHONPATH
- copy the script to place of your script

# Usage
## As a script
- ### creating basis sets
```
python basis_generator.py
```
This will create octahedron basis sets written as a json file inside the `basis` directory.
The repository already includes this output.
- ### projection onto the basis set
```
python polyhedron_analysis.py POSCAR n
```
where POSCAR is [VASP](https://www.vasp.at/) POSCAR and n is n-th atom in the centre of the octahedron.
Use the API for other input types.

## As an API
- see [Tutorial notebook](https://github.com/KazMorita/polyhedron_distortion/Tutorial1_API.ipynb)

# Citation
See the following paper for the theoretical background.
K. Morita, D. W. Davies, K. T. Butler and A. Walsh, "Breaking the aristotype: featurisation of polyhedral distortions in perovskite crystals" (link to be added)

