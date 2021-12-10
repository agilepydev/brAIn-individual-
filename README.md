# brAIn

## Description
Acme Corporation is a worldwide supplier of technological equipment. The factory is facing significant problems with their manufacturing line, the machines are constantly facing failures due to a lack of maintenance and the production is stopped every time an unexpected failure is presented. As a result, Acme is losing millions of U.S. Dollars and important clients like Wile E. Coyote are experiencing delays in deliveries.

The company has collected audio samples of equipment working on normal and anomalous conditions. Their objective is to develop a machine learning model able to monitor the operations and identify anomalies in the sound pattern.

![App Screenshot](https://github.com/agilepydev/brAIn-individual-/blob/development/assets/brain.png)

The implementation of this model can allow Acme to operate the manufacturing equipment at full capacity and detect signs of failure before the damage is so critical that the production line has to be stopped.

Our mission is to build a machine learning model for Acme, so they can continue their manufacturing activities and help the Coyote to catch the roadrunner.


## Objectives

- Individual execution
- Leverage your work on the previous data exploration
- Provide a new Github repo with a clear readme file
- Present a short report with recommendations and conclusions:
- Data visualization
- ML model for classification, metrics and overall performance.
- Selected metric and why is that the right metric
- Limitations of your model & feasibility of implementation
- Unsupervised learning: data exploration and results
- Feasibility of labeling the data using clusters (Failure mode & machine type)
- What conditions are common to a cluster? What is characterizing that cluster?
- Insights that we cannot see on the data using classification
- Any outliers? Why ?


## Repo architecture

* README.md -> Explains the project and gives a report

* requirements.txt -> Shows information on what libraries and oython version to install/use.

* Clustering.ipynb  -> The file with all the code.

* all_decibel00.csv -> The dataframe used for the clustering project.

* finalize_model.pkl -> The finalized model as pkl


## Installation

`git clone` this repository into your local environment. 

Link to the datasets used in this project:

* [Machine Condition Monitoring](https://zenodo.org/record/3384388#.YFIrNXnvJEY)

In the [requirements.txt]('https://github.com/agilepydev/brAIn-individual-/blob/development/requirements.txt') file you can find all the necessary libraries to install and what python version to use.

## Usage

By reading the readme file you're able to get a clear description of the objective and final report on the sound project for Acme executed on the Clustering.ipynb file.

## Timeline

*October - November 2021*

- Duration: `3 days`
- Deadline: `10/12/21 16:00 PM`

## Report

### Classification

#### Preprocessing

As in the first stage of the project together with my colleague [N1chelle](https://github.com/N1chelle) 
we installed the datasets from each machine with the decibel number zero.
We extracted our files based on these six features: ![features](https://github.com/agilepydev/brAIn-individual-/blob/development/assets/features.png?raw=true)
We were able to plot the spectogram wich gives us Insights on the amount of hertz per certain timeframes wich effects the number of decibels.
![spectogram](https://github.com/agilepydev/brAIn-individual-/blob/development/assets/spectogram.png?raw=true)
This plot gives us insights on the signal based on the Amplitude per few samples of each timeframe.
![signal](https://github.com/agilepydev/brAIn-individual-/blob/development/assets/amplitude.png?raw=true)

This specific plot shows that the rate of the amplitude increased based on how low the frequency bin of the sound spectrum.

![spectrum](https://github.com/agilepydev/brAIn-individual-/blob/development/assets/amplitude_frequency.png?raw=true)

This shows the correlation of each feature:

![corr](https://github.com/agilepydev/brAIn-individual-/blob/development/assets/correlation.png?raw=true)

#### Models

We have experimented with 3 different models, our main metric was accuracy and this is how the mdoels performed:

KNN: 90.8%

Random Forest: 94.4%

SVM: 78.3 %

These are the extra metrics:


### Clustering

For the unsupervised aspect of this project both me and my colleague worked individually, and I used the dataset that I extracted previously.

For the clustering I decided to work with the K-Means model, to get a better overview of the data I clustered I made the following plot:

![pairplot](https://github.com/agilepydev/brAIn-individual-/blob/development/assets/pairplot.png?raw=true)


As for the identification of the abnormal, normal & transitory clusters I made the following plot.

![first_cluster](https://github.com/agilepydev/brAIn-individual-/blob/development/assets/zero_crossing_clusters.png?raw=true)

As it wasn't too accurate to wich color belongs to what cluster I made a comparison of the previous and the clustered dataset.

![clusters](https://github.com/agilepydev/brAIn-individual-/blob/development/assets/clusters.png?raw=true)

Since previously we defined abnormality as 1 and normality as 0 in the classes and as we can see those clusters have the same value so we can assume that number two is the transition stage, also on the previous visual we could see that number 2 was in between 1 & 0 wich really defines as a transition, only now we were actually able to prove it.

Note: For Clusters (0= normality, 1= abnormality, 2= transitory)

For the visualization of the distortions of K-Means I decided to plot a graph using the elbow method.

As for the metric scores K-means, this is the performance:

The Silhouette Coefficient: 0.55

Calinski-Harabasz Index (Variance Ratio Criterion): 12587.63

Davies-Bouldin Index: 0.55

I also managed to save the model to disc as a .pkl file and you can find this in the repository.

I was also able to work with the DBSCAN method wich I should work more on as the visualization on this isn't too clear.

![not_clear](https://github.com/agilepydev/brAIn-individual-/blob/development/assets/DBSCAN.png?raw=true)


If any of this wasn't too clear feel free to include your engineers or contact our support team.


## Personal situation
I'm currently participating in the [Becode.org AI Bootcamp](https://becode.org/learn/ai-bootcamp/) to upskill into a career in data science. 

## Contributors
[agilepydev](https://github.com/agilepydev)


