# TECH-3D & eTECH-3D

This repository contains our implementation for chromatin 3D inference from Hi-C data using deep learning. A detailed description of the project can be found in `root -> report -> written_report -> master_thesis_report.pdf`. 

## Repository Organisation

* `tech3d`: contains the implementation of TECH-3D (**T**ransfer learning **E**ncoder for **Ch**romatin **3D** structure prediction) for different encoders (Linear or Bi-LSTM) and train datasets (Synthetic Random Walk Structures or Synthetic Biological Structures). To run the code, one need to:
    1. Generate the synthetic train data by running the appropriate data generator (e.g. `data_generation -> synthetic_random_trussart_data_generation.ipynb`). 
    2. Train the network on the previously generated data by running the appropriate notebook (e.g. `networks -> synthetic_random_trussart -> linear -> synthetic_random_trussart_linear.ipynb`).

   In the example above, TECH-3D is designed the for test [Trussart](http://sgt.cnag.cat/3dg/datasets/) Hi-C matrix  at 5Kb, i.e. the generated synthetic structures and contact matrices have 202 bins. A similar implementation for other test datasets ([GEM12878](http://sysbio.rnet.missouri.edu/3dgenome/GSDB/) and [Fission Yeast](http://sysbio.rnet.missouri.edu/3dgenome/GSDB/)) is also available. 

* `etech3d`: contains the implementation of eTECH-3D (**e**nsemble-based **T**ransfer learning **E**ncoder for **Ch**romatin **3D** population of structures analysis). As for TECH-3D, eTECH-3D uses transfer learning and the working pipeline is similar as above. 

* `experiments`: contains the experiments evaluating both TECH-3D and eTECH-3D as well as benchmark algorithms ([REACH-3D](https://arxiv.org/abs/1811.09619), [GEM](https://biologicalproceduresonline.biomedcentral.com/articles/10.1186/s12575-019-0094-0) and [miniMDS](https://academic.oup.com/bioinformatics/article/33/14/i261/3953988)). All the experimental figures of the report can be regenerated from the jupyter notebooks in this folder. 

* `previous_works`: contains the implementations of [REACH-3D](https://arxiv.org/abs/1811.09619), [GEM](https://biologicalproceduresonline.biomedcentral.com/articles/10.1186/s12575-019-0094-0) and [miniMDS](https://academic.oup.com/bioinformatics/article/33/14/i261/3953988) as well as data formatters designed to transform the Hi-C contact map (e.g. the Trussart contact map at 5Kb) into the required format. For GEM and miniMDS, the implementation is obtained from the official repository. On the other hand, REACH-3D was developed from scratch in [Pytorch 1.9.0](https://pytorch.org/)  (originally in [Tensorflow 1.9.0](https://www.tensorflow.org/)).

* `report.zip`: contains all the literature covering TECH-3D and eTECH-3D. 

## Installation

First, clone the repository. Then, we recommend to work in a separate python environment. For this, run the following command at the root (use the package manager [pip](https://pip.pypa.io/en/stable/) to install python `venv`, if required):

```bash
python3 -m virtualenv tech3d_venv
source tech3d_venv/bin/activate
```
Finally, install the required libraries:

```bash
pip3 install -r requirements.txt
```

## Notes

* In the code, it is possible that the name tREACH-3D is used instead of TECH-3D. This is because the name of our framework changed lately. Similarly, eTECH-3D can be referred as tCev-3D.
* In the repository, data files and external repositories are compressed for memory space efficiency. We recommend to unzip the files before working on the code.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)