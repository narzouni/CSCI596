# CSCI596 Final Project

## The association of Obstructive Sleep Apnea Syndrome (OSAS) with Cognitive Impairment and Dementia.

<br/><br/>


## Study Goals/Objectives:

+ The purpose of the study is to compare the predicted brain biological age with the true chronological age of subjects with OSA and MCI (Mild Cognitive Impairment). 

+ The main hypothesis to test is: If OSA with CI patients show similar aging patterns and morphological changing, this can signify that OSA CI is a subtype of MCI that may lead to Dementia if left without treatment.

<br/><br/>

## Datasets:

+ I am using SMC (Samsung Medical Center) data for OSA, ADNI, and ICBM. Some OSA subjects may have Cognitive Impairment (CI) and some don’t have CI. I will be using ADNI MCI (Mild Cognitive Impairment) and Control healthy subjects. I will be using control healthy subjects from ICBM.

+ I am using Males in the analysis because females may have many complications that affect their sleep patterns.

+ I am using MRI T1 weighted Images in addition to some measures like Cognitive scores for OSA. The MRI images will be used to extract features on the brain.

+ There are 59 OSA without cognitive impairment and 17 OSA subjects with CI. 

+ There are 23 Normal OSA subjects with feature files.

+ There are 152 ADNI CN male subjects with feature files.

+ There are 44 ICBM CN male subjects with feature files.

+ There are 390 ADNI MCI male subjects with feature files.

<br/><br/>

## Machine Learning Methods:

+ The irregular domain of the brain is changed into a graph. I am using GCN (Graph Convolutional Neural Network) using `Python`. Each subject’s brain will be
represented by a graph of around 100K nodes. At each node some morphological brain measures are calculated.

+ The GCN model is trained using the control healthy subjects (23 Normal OSA + 152 ADNI CN Male + 44 ICBM Males). The total number of CN subjects for training is 219 subjects.

+ The trained model is tested on the three test groups: OSA with CI, OSA without CI, and ADNI MCI.

+ I am using two features cortical thickness, and grey matter white matter ratio.
<br/><br/>
![Brain](https://github.com/narzouni/CSCI596/blob/main/brainnetwork.bmp =100x)

