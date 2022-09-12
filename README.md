<h1> Note </h1>

This is a MSR study as part of the MSR course 2022 at UniKo, CS department, SoftLang Team

<h2> Names of team/students </h2>

**Team Name**: Kilo

**Members:**

  * Ahmed Fazal (afazal@uni-koblenz.de)
  * Usama Moin (umoin@uni-koblenz.de)
  * Tahir Iqbal (tahiriqbal@uni-koblenz.de)

<h2> Underlying paper </h2>

The DBLP Link for the Paper used in this Assignments is as follows:

<https://dblp.org/rec/conf/msr/YoungCMTHB21.html>

<h2> Reproduced baseline  </h2>

### Objective of reproduction 
 
* #### Description: 

This paper characterizes contributor acknowledgment models in open source by analyzing thousands of projects that use a model called All Contributors. It focuses on the life cycle of projects through the model's lens and contrast its representation of contributorship. We would be reproducing the data pipeline for the list of contributors and contribution history
      

* #### Input data

The input data is extracted from GitHub API consisting of:

- Forked results and fork parents
- Repositories list and shortlisted repositories list
- Contributors list and size

The link to the Input Data for Team Kilo's Git Project is as follows:

<https://github.com/afazal/Team_Kilo_Poject_MSR/tree/main/data/sample%20data>


* #### Output data


The output we get from the executions is similar to the one done by the original author of the paper
Implementation of reproduction.

The link to the Output Data for Team Kilo's Git Project is as follows:

<https://github.com/afazal/Team_Kilo_Poject_MSR/tree/main/data/output%20data>


<h3> Findings </h3> 
 
* #### Process delta:

The process we followed for the project is almost identical to the one the author followed except in some cases we had to change libraries since the previous ones are deprecated or no longer functional. Moreover we did some optimisations as well. For the purpose of replication in some cases we had to use similar data as was used by the author since github rate limits you after a while unless you have an academic or research license.



* #### Output delta:

The output we get from the executions is almost similar to the one done by the original author of the paper. The visualizations that we have generated from our dataset matches the output visuals that are provided in the paper. The few differences are due to the formatting of the dataset as well as randomized github api calls for generating the dataset.


<h2> MSR study enhancement </h2>

* #### Threat 

From the model of acknowledgement of Github contributorship, only a small sample from among the overall projects is used. The current contributorship does not take into account the the list of github datasets wihout contributors which creates a problem.


* #### Traces 

“Our sample is biased towards projects willing to go out of their way to acknowledge contributors using a method that is not widely used, which is a particularly prosocial behavior. Hence, the group of acknowledged the contributors might be particularly broad relative to a typical OSS project”. 

“The code that appears on GitHub is itself a skewed sample of OSS software so our results might not generalize to other services or populations” [18].   

"On a technical note, we have filtered bots using simple pattern matched on names combined with a hand-crafted list of bots. More exhaustive filtration techniques could reduce this threat in the future" [41]

* #### Theory 

This is a threat because the other projects that acknowledge the contributors using a less widely used method are not taken into consideration which creates a bias in the results. The github code are from the sample of OSS software which may not take other services into consideration. Also, there is an assumption that each contributor logins are a single user, but they could be instances where user names are provided without login.

* ####  Methodology 
— Describe your planned methodology.

* #### Feasibility 
— What concessions did you make so that the experiment fits in this course?

* #### Process 
— Extra process, on top of baseline.

* #### Data 
— Extra data, on top of baseline.

* #### Results 
— What are you findings / your interpretation of your results?


<h2> Implementation  </h2>

 #### Hardware requirements 

* Windows:

    - Processor: Intel i5-6600k (4 core 3.3 GHz) or AMD Ryzen 5 2400 G (4 core 3.6 GHz)
    - RAM: 8.00 GB
    - System type: 64-bit operating system, x64-based processor
    - Operating System: Windows 10

* Apple:

    - Model: MacBook Pro (13-inch, 2020, Four Thunderbolt 3 ports)
    - Processor: 2 GHz Quad-Core Intel Core i5
    - RAM: 16.00 GB
    - System type: 64-bit operating system, x64-based processor
    - Operating System: macOS Monterey Version
    - Graphics: Intel Iris Plus Graphics 1536 MB
       


#### Software requirements 

* Framework
  - Jupyter Notebook or Spyder IDE
  - PyGithub
  - python 3.8

* Libraries
  - pandas
  - matplotlib
  - wget
  - random
  - requests

#### Data: 
We have used the sample dataset provided by the paper resource on figshare.com as the implementation. The relevant data files used can be found in the ./data folder







