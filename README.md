# Developing Predictive Oil Well Diagnostics Based on Intelligent Algorithms
[![PWC](https://img.shields.io/badge/PyTorch-v1.8-red)](https://pytorch.org/)

> **Developing Predictive Oil Well Diagnostics Based on Intelligent Algorithms**<br>
> [Zhanar Omirbekova](),
> [Daur Aktaukenov](),
> [Aslan Amangeldiyev](),
> [Abdelrahman Abdallah](https://github.com/abdoelsayed2016),
> <br>

## Abstract 

The current competitive market condition in the oil industry is so concentrated on companies' budgets that they require methods to extract oil from wells at the lowest possible cost. All pumping units, new or old, require regular preventive maintenance and constant inspection, and with 30 percent of total oil production coming from sucker rod pumps, the cost of diagnostics must be reduced accordingly.This article focuses on the intelligent diagnostics of the rod and borehole pump for preventive maintenance and monitoring during the life cycle of the well. The use of artificial intelligence methods for predictive diagnostics of equipment condition solves problems without production stoppages and without additional interventions from outside.





### requirements:

**Machine Learing and Plot Packages**

```pip install -r requirements.txt```

**Pytorch**

for deep learning you should install pytorch 1.6.0 


### generate RTF data:

    python ./pdm.py inputs_rtf.py

### Build the Model in Jupyter notebook

```
>>> jupyter notebook
```

### execute PdM simulation:

Now that the PdM models have been built, execute the simulation again but in PdM mode:

    python pdm.py inputs_pdm.py





 



### next steps:

1. add deep learning models 

2. tailor pdm_threshold_time so that different values can be used by the 3 different models
 



## Cite as
If you find this work useful for your research, please cite our paper:
```
@INPROCEEDINGS{9465959,
  author={Omirbekova, Zhanar and Aktaukenov, Daur and Amangeldiyev, Aslan and Abdallah, Abdelrahman},
  booktitle={2021 IEEE International Conference on Smart Information Systems and Technologies (SIST)}, 
  title={Developing Predictive Oil Well Diagnostics Based on Intelligent Algorithms}, 
  year={2021},
  volume={},
  number={},
  pages={1-7},
  doi={10.1109/SIST50301.2021.9465959}}
```





### Reference 
[1] https://github.com/joehahn/predictive-maintenance-sim
[2] https://www.datascience.com/blog/predictive-maintenance-for-upstream-oil-and-gas
