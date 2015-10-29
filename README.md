This repository contains information related to the tool EVOSS presented in ICSE, 2012. The tool was originally presented in [this paper](http://dl.acm.org/citation.cfm?id=2337433)

This repository _is not_ the original repository for this tool. Here are some links to the original project:
* [The Official Project Page, including source code](http://evoss.di.univaq.it/)
* [A Video of the Tool](http://www.di.univaq.it/diruscio/sites/evoss/docs/video.htm)

In this repository, for EVOSS you will find:
* :white_check_mark: [Source code]( http://code.google.com/p/ mancoosi-uda/source/checkout) (available)
* :white_check_mark: [The original tool](https://code.google.com/p/mancoosi-uda/downloads/detail?name=all-evoss.tar.gz&can=2&q=) (available)

This repository was constructed by [Pankti Desai](https://github.com/panktidesai) under the supervision of [Emerson Murphy-Hill](https://github.com/CaptainEmerson). Thanks to Davide Di Ruscio, Patrizio Pelliccione and Alfonso Pierantonio for their help in establishing this repository.



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
