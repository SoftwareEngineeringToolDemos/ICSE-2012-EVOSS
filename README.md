This repository is contains information related to the tool EVOSS presented in ICSE, 2012 . Link to paper : http://dl.acm.org/citation.cfm?id=2337433

This repository is not the original repository for this tool. Here are some links to the original project:
* http://code.google.com/p/ mancoosi-uda/source/checkout
* https://github.com/davidediruscio/evoss
* [A video of the tool](http://www.di.univaq.it/diruscio/sites/evoss/docs/video.htm)

This repository was constructed by [Esha Sharma](https://github.com/eshasharma) under the supervision of [Emerson Murphy-Hill](https://github.com/CaptainEmerson). Thanks to Apoorv Mahajan , Pankti Desai , Dheeraj Shetty for their help in establishing this repository.



# EVOSS

EVOSS implements a model-based approach to support the upgrade of FOSS
systems. The approach promotes the simulation of upgrades to predict failures before
affecting the real system. Both fine-grained static aspects (e.g. configuration incoher-
ences) and dynamic aspects (e.g. the execution of configuration scripts) are taken into
account, improving over the state of the art of package managers. 

[http://mancoosi-uda.googlecode.com/files/approach.PNG]


An overview of the EVOSS approach is sketched in the figure. The simulation of a system upgrade is performed by the Upgrade Simulator which takes a set of models as input produced
by the Injector: a System Configuration Model and Package Models corresponding to
the packages which have to be installed/removed/replaced. The output of Upgrade Simulator is a new System Configuration Model if no errors occur during the simulation,
otherwise an Incoherences Report is produced. The new System Configuration Model is
queried and analyzed by the Failure Detector component. When Failure Detector discovers inconsistencies they are collected in the Incoherences Report. The real upgrade is
performed on the system only if the new system configuration model is coherent.

For more information please refer to http://dx.doi.org/10.1016/j.scico.2010.11.001 or http://mancoosi-uda.googlecode.com/files/scp_draft.pdf or http://evoss.di.univaq.it/
