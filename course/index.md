# Data Engineering for Machine Learning

##  Overview

*Data Engineering for Machine Learning* is a novel course at the intersection of Systems, Big Data and Machine Learning. The course focuses on **machine learning systems in the real-world**, as well as on **data-related problems** that typically occur in end-to-end machine learning deployments. The lectures cover systems deployed in practice at companies like Google, Twitter & Amazon, and research from a variety of conferences such as [NeurIPS](https://nips.cc/) (ML), [VLDB](hhttps://vldb.org/2019/) / [SIGMOD](https://http://sigmod2019.org/) (data management) and [OSDI](https://www.usenix.org/conference/osdi18) (systems). Students will learn about **abstractions and concepts of ML-related systems** on the on hand, and gain **practical experiences in use cases such as data and model validation, experiment databases, and data cleaning** on the other hand.

This course will be taught by [Sebastian Schelter](https://ssc.io), an MSDSE Fellow at CDS. Sebastian has already gained a lot of practical experience in real-world ML systems, as an intern with the [recommender systems team at Twitter](https://ssc.io/pdf/factorbird.pdf), and as a Senior Applied Scientist at [Amazon Core AI Berlin](http://www.vldb.org/pvldb/vol11/p1781-schelter.pdf), where he spent three years before joining NYU. He is a committer and PMC member in several systems-related projects of the [Apache Software Foundation](https://apache.org). Additionally, he mentors the deep learning-related project [Apache TVM](https://tvm.ai) for the Apache Incubator, and is the creator and chair of the workshop series on ['Data Management for End-to-End Machine Learning'](http://deem-workshop.org) at ACM SIGMOD.


## Preliminary Syllabus

### Introduction

#### 09/05 - Real-World Machine Learning Systems

*end-to-end machine learning systems in the real-world; ML engineering; anecdotes; open problems and challenges*

* Sculley et al.: [Hidden Technical Debt in Machine Learning Systems](https://papers.nips.cc/paper/5656-hidden-technical-debt-in-machine-learning-systems.pdf), NeurIPS'15 <br/>
* Polyzotis et al.: [Data Management Challenges in Production Machine Learning](https://dl.acm.org/citation.cfm?id=3035918.3054782), SIGMOD Record'18
* Schelter et al.: [On Challenges in Machine Learning Model Management](http://sites.computer.org/debull/A18dec/p5.pdf), IEEE Data Engineering'18

---

#### 09/12 - Systems Foundations

*history of large-scale data processing; systems basics: data parallelism, task parallelism, pipeline parallelism; memory hierarchy; end of Moore's law; distributed filesystems; machine learning in practice; machine learning engineering*

* Drepper: [What every programmer should know about memory](https://people.freebsd.org/~lstewart/articles/cpumemory.pdf), 2007
 * Ghewamat et al.: [The Google Filesystem](https://storage.googleapis.com/pub-tools-public-publication-data/pdf/035fc972c796d33122033a0614bc94cff1527999.pdf), SOSP'03
 * Zinkevich: [Rules of Machine Learning: Best Practices for ML Engineering](https://developers.google.com/machine-learning/guides/rules-of-ml/)

---

### Systems for Machine Learning

#### 09/19 - Machine Learning on Distributed Dataflow Systems I

*recap: abstractions for parallel data processing (MapReduce / Resilient Distributed Datasets); reformulation of ML algorithms using MapReduce; SparkML*

 * Dean et al.: [MapReduce: Simplified Data Processing on Large Clusters](https://www.usenix.org/legacy/events/osdi04/tech/full_papers/dean/dean.pdf), OSDI'04
 * Chu et al.: [Map-Reduce for Machine Learning on Multicore](http://papers.nips.cc/paper/3150-map-reduce-for-machine-learning-on-multicore.pdf), NeurIPS'07
 * Zaharia et al.: [Resilient Distributed Datasets: A Fault-Tolerant Abstraction for In-Memory Cluster Computing](https://www.usenix.org/system/files/conference/nsdi12/nsdi12-final138.pdf), NDSI'12
 * Meng et al.: [MLlib: Machine Learning in Apache Spark](http://www.jmlr.org/papers/volume17/15-237/15-237.pdf), JMLR'16

---

#### 09/26 - Machine Learning on Distributed Dataflow Systems II

*domain-specific languages for ML; compilation of ML programs to dataflow systems; limits of scalability; performance issues of distributed dataflow systems*

 * Böhm et al.: [SystemML: Declarative Machine Learning on Spark](http://www.vldb.org/pvldb/vol9/p1425-boehm.pdf), VLDB'16
 * Zhang et al.: [DimmWitted: A Study of Main-Memory Statistical Analytics](https://arxiv.org/pdf/1403.7550.pdf), VLDB'14

---

#### 10/03 - Distributed Learning with Parameter Servers

*scalable asychronous learning; Hogwild!-style SGD; limitations of distributed learning; distributed matrix factorization*

 * Dean et al.: [Large Scale Distributed Deep Networks](http://papers.nips.cc/paper/4687-large-scale-distributed-deep-networks), NeurIPS'12
 * Li et al.: [Scaling Distributed Machine Learning  with the Parameter Server](https://www.usenix.org/system/files/conference/osdi14/osdi14-paper-li_mu.pdf), OSDI'14

--- 
 
#### 10/10 - Deep Learning Engines

*representation of deep neural networks as computational graphs; auto-differentiation; scheduling of mini-batch SGD; eager execution; optimization for CPU/GPU; deep learning compilers*

 * Abadi et al.: [TensorFlow: A System for Large-Scale Machine Learning](https://www.usenix.org/system/files/conference/osdi16/osdi16-abadi.pdf), OSDI'16
 * Chen et al.: [MXNet: A Flexible and Efficient Machine Learning Library for Heterogeneous Distributed Systems](https://www.cs.cmu.edu/~muli/file/mxnet-learning-sys.pdf), ML Systems workshop at NeurIPS'15
 * Chen et al.: [TVM: An Automated End-to-End Optimizing Compiler for Deep Learning](https://www.usenix.org/system/files/osdi18-chen.pdf), OSDI'18

---

#### 10/17 - Model Serving Systems 

*model serving; deploying machine learning models; A/B tests*

 * Crankshaw et al.: [Clipper: A Low-Latency Online Prediction Serving System](https://www.usenix.org/system/files/conference/nsdi17/nsdi17-crankshaw.pdf), NSDI'17
 * Olson et al.: [Tensor Flow-Serving: Flexible, High-Performance ML Serving](http://learningsys.org/nips17/assets/papers/paper_1.pdf), ML Systems workshop at NeurIPS'17
 * Kohavi et al.: [Practical Guide to Controlled Experiments on the Web: Listen to Your Customers not to the HiPPO](https://courses.cs.washington.edu/courses/cse454/15au/papers/p959-kohavi.pdf), KDD'07
 
---

### Data Management for Machine Learning 

#### 10/24 Model and Metadata Management

*experiment databases; managing models and metadata in ML experiments; reproducibility in ML; collaboration between data scientists*

 * Vanschoren et al.: [OpenML: networked science in machine learning](https://arxiv.org/pdf/1407.7722.pdf), KDD'14
 * Vartak et al.: [ModelDB: Opportunities and Challenges in Managing Machine Learning Models](http://sites.computer.org/debull/A18dec/A18DEC-CD.pdf#page=18), IEEE Data Engineering'18
 * [Databricks MLflow](https://www.mlflow.org/)

---

#### 10/31 Automated Machine Learning

*automating supervised learning; accelerating model selection; relationship between query optimization and model search*

  * Feurer et al.: [Efficient and Robust Automated Machine Learning](http://papers.nips.cc/paper/5872-efficient-and-robust-automated-machine-learning.pdf), NeurIPS'15
  * Binnig et al.: [Towards Interactive Curation & Automatic Tuning of ML Pipelines](https://par.nsf.gov/servlets/purl/10066177), DEEM workshop at SIGMOD'18

---

#### 11/07 Data Validation and Data Cleaning

*data quality dimensions; data profiling; data cleaning; unit tests for data; constraint suggestion; anomaly detection; missing value imputation*

 * Hellerstein: [Quantitative Data Cleaning for Large Databases](http://db.cs.berkeley.edu/jmh/papers/cleaning-unece.pdf), 2002
  * Schelter et al.: [Automating Large-Scale Data Quality Verification](http://www.vldb.org/pvldb/vol11/p1781-schelter.pdf), VLDB'18
 * Biessmann et al.: [Deep Learning for Missing Value Imputation in Tables with Non-Numerical Data](https://ssc.io/pdf/p2017-biessmann.pdf), CIKM'18
 
--- 
 
#### 11/14 Model Validation

*operating ML systems; schema-validation of features; dataset shift detection;*

 * Baylor et al.: [TFX: A TensorFlow-Based Production-Scale Machine Learning Platform](http://stevenwhang.com/tfx_paper.pdf), KDD'17
 * Breck et al.: [The ML Test Score: A Rubric for ML Production Readiness and Technical Debt Reduction](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8258038), BigData'17 
 * Rabanser et al.: [Failing Loudly: An Empirical Study of Methods for Detecting Dataset Shift](https://arxiv.org/pdf/1810.11953.pdf), 2019
 
---

#### 11/21 Fairness in Automated Decision Making

*fairness and bias in ML; measuring fairness; counter measures*

  * Barocas et al.: [Big Data's Disparate Impact](http://www.californialawreview.org/wp-content/uploads/2016/06/2Barocas-Selbst.pdf)  
  * Dwork et al.: [Fairness Through Awareness](https://arxiv.org/pdf/1104.3913.pdf), FAT*ML'12
  * Kamiran et al.: [Data preprocessing techniques for classification without discrimination](https://link.springer.com/content/pdf/10.1007%2Fs10115-011-0463-8.pdf), 2012

---

#### 11/28 __Thanksgiving__

---

### Case Studies  

#### 12/05 Case Study: Large-Scale Demand Forecasting at Amazon

*analysis of a real-world end-to-end ML system from Amazon*

 * Böse et al.: [Probabilistic Demand Forecasting at Scale](http://www.vldb.org/pvldb/vol10/p1694-schelter.pdf), VLDB'17
 * Salinas et al.: [DeepAR: Probabilistic Forecasting with Autoregressive Recurrent Networks](https://arxiv.org/pdf/1704.04110)
 
---

#### 12/12 Invited Guest Lecture with Industry Practitioner
 
---
  
#### 12/19 Final Exam
