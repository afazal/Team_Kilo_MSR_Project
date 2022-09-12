<h1> Objective of Reproduction </h1>

The objective of this reproduction is to test whether the analysis of the contributorship mentioned in the paper can be reproduced and if similar results can be obtained while using various repositories.

<h2>Description</h2>

This paper characterizes contributor acknowledgment models in open source by analyzing thousands of projects that use a model called All Contributors. It focuses on the life cycle of projects through the model's lens and contrast its representation of contributorship. We would be reproducing the data pipeline for the list of contributors and contribution history.

<h2>Input data</h2>
The input data is extracted from GitHub API consisting of:

- Forked results and fork parents
- Repositories list and shortlisted repositories list
- Contributors list and size
- We characterize contributor acknowledgment models in open source, analyze the life cycle of projects through different models.
- Findings of reproduction
- Process Delta
- The process we followed for the project is almost identical to the one the author followed except in some cases we had to change libraries since the previous ones are deprecated or no longer functional. Moreover we did some optimisations as well. For the purpose of replication in some cases we had to use similar data as was used by the author since github rate limits you after a while unless you have an academic or research license.

<h2>Output data</h2>

- The output we get from the executions is similar to the one done by the original author of the paper
Implementation of reproduction.




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
  - pandas
  - matplotlib
  - Validation
  - To verify the output, it is best to open the generated files and go through the results in "data/" folder.

#### Data: 
We have used the sample dataset provided by the paper resource on figshare.com as the implementation. The relevant data files used can be found in the ./data folder





<h2> Names of team/students </h2>

**Team Name**: Kilo

**Members:**

  * Ahmed Fazal (afazal@uni-koblenz.de)
  * Usama Moin (umoin@uni-koblenz.de)
  * Tahir Iqbal (tahiriqbal@uni-koblenz.de)

<h2> Underlying paper </h2>

— DBLP link

<h2> Reproduced baseline  </h2>

### Objective of reproduction 
 
* #### Description

    (1-2 sentences) 
  — What is actually reproduced? (What part of the study?)
  
* #### Input data

(1+ lines) 
— provide links to the paper’s repo, if possible, and to your git project.

* #### Output data

(1+ lines) 
— provide links to the paper’s repo, if possible, and to your git project.

<h3> Findings </h3> 
 
* #### Process delta:

How does your process differ from what’s described in the paper or its repo? (Why?)

* #### Output delta:

How does your output differ …? (What’s the significance of any differences observed?)


<h2> MSR study enhancement </h2>

* #### Threat 
— Call out the threat to validity.

* #### Traces 
— Identify traces (quotes/references) in the paper related to the threat.

* #### Theory 
— Describe your theory as to why this is a threat.

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

