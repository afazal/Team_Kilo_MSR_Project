
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

The input data is extracted from Github Archive consisting of:
- All the actions performed on github including Commit, Push, etc along with details about the repositories involved.
The process to generate the input data is included in python code, we didn't include it in the github project due to the size of the input files.

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
The original study focused on repositories having ._all_-_contributorsrc_ file, so it was missing out on a huge chunk of open source software repositories which did not include this file as a result the results don't cover the trends over all of github. To bypass that we started by randomly selecting some repositories which were active during the year 2021, performed analysis on that data and extracted list of contributors along with their basic details against each repository and then compared the results with that in the original paper.

* #### Feasibility 
Extracting data and performing analysis on the data extracted from github is a big data problem which requires expensive resources with high computing powers, as the data involving number of actions performed in github during a single hour can take a minimum of 50mb and a maximum of 10 gb data. To make the problem simpler instead of gathering all those data and performing analysis on a personal computer, we went ahead and randomly sampled the data for the year 2021 in order to extract a small dataset to study the trends.

* #### Process 

The baseline approach made use of the same coding scripts and focused on the same steps as used by the authors of the Paper. The data used in the baseline approach was a similar type of data that our team extracted separately. The enhacement process focuces on a different aspect of the baseline approach. Here we have employed the use of our own data analysis script, which works on randomly sampled "Repository" data which we then use to extract contributors list instead of a systematically built "All contributors List" as was used by the authors of the paper.

* #### Data 

We have extracted the data from data dump <https://data.gharchive.org/> (commands like wget to get the https data) which are essesntially compressed json files. We then used the python code to extract the repositories with the contributors list and randomly selected some of them to remove biases. The data is then further analysed to produce visuals, predominantly the bar chart (included in the "contributors.ipynb" file in process folder) which act as a benchmark comparison between the data output done in the paper and the reproduced study.

* #### Results
Our initial assumption was that we would observe a different trend when randomly selecting repositories as compared to author's approach of selecting repositories with  ._all_-_contributorsrc_ since small repositories don't generally use   ._all_-_contributorsrc_  but our output when plotted in graphs present almost the same visual image as that of the authors. Within the limited computing power that we had we can conclude that author's analysis provide the correct image of contributors throughout the github and is not limited to a subset containing  ._all_-_contributorsrc_ file.

![ContributionsGraph](https://user-images.githubusercontent.com/8388775/189758463-28902cbd-701d-460d-b5b2-251e5f46f36e.png)



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

