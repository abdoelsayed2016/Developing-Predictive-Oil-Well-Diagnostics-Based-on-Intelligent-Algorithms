# predictive maintenance sim 

  




by Abdelrahman Abdallah,<br />
this repo is python3 version of https://github.com/joehahn/predictive-maintenance-sim

The python codes and Jupyter notebooks provided here are used to
simulate a Predictive Maintenance (PdM) strategy 
applied to a suite of 1000 virtual oil & gas wells. A simple toy-model approach is used here, 
to simulate the production variations that real wells might experience
as they operate over time. Each simulated well has three virtual sensors that measure three mock quantities:
pressure P, temperature T, and load L.
As time advances, a well's P,T,L settings slowly random-walk away 
from the well's sweet-spot, which is where well production is highest and faults are rarest.
And as a well random-walks further from the sweet spot, it becomes ever more likely to suffer a failure,
which then zeros the failed well's production as it waits for the next
available technician to service it. And when the technician does complete the repair,
that well's P,T,L settings are then returned to its sweet spot, and production resumes. Note that
this simulation also has a limited pool of virtual technicians, and if technicians become 
oversubscribed by failed wells, then
the next failed well must wait until a tech completes the current repair before servicing
the next failed well, and such bottlenecks can result
in a considerable loss of production. Simulated 
wells are also subject to three possible mock faults: a jammed_rotor, cracked_valve, or broken_gear, and every 
tech that diagnoses a failed well also notes that diagnosis in repair log.

The simulation is initially executed in run-to-fail (RTF) mode, which means that wells are
serviced only after experiencing a failure, and the purpose of the RTF simulation is to generate
a large pile of telemetry and repair data. Machine learning (ML) models are then trained on the
telemetry + repair logs, to predict which operating wells are likely to fail soon. After the ML models
are built, the following then reruns this simulation in PdM mode, which uses those ML models to flag those
wells that are likely to fail soon, and then assigns available service technicians to perform
preventative maintenance on the flagged wells. After the PdM simulation is complete,
a Jupyter notebook loads the PdM output to assess how the suite of simulated wells'  
production is boosted by the PdM strategy, and how PdM also impacts the technicians'
utilization.

See also my blog post on this topic at 
https://www.datascience.com/blog/predictive-maintenance-for-upstream-oil-and-gas

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
 







