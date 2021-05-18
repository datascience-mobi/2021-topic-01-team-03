# Cleaning

## Selecting brain cancer specific cell lines in all data sets
- Find out in *prism.cl* what are the names of the brain cancer cell lines and save them as a vector *names*
- Using this new vector we select the brain cancer cell lines from other dataframes and save them as new ones. For example *prism.cnv* would become *brain_cancer_cnv*

## NA removal from brain_cancer_achilles
- Achilles dataset contains information about gene KO. However some of the brain cancer cell lines do not have information about KO at all. In other words in *brain_cancer_achilles* some cell lines have entire row of NAs
- We remove such cell lines 

## NA for mean substituition in brain_cancer
- In this dataset columns represent drugs in different assays and concentrations, basically column = experiment on every cell line
- There are many NAs in columns (no information how did the experiment go for some cell lines)
- We cannot remove the entire columns because we would lose a lot of information, so we substitute all the NAs for the mean of the column
- However, there are a few columns left that only have NAs. So the substitution for mean did not work there, since there are not any values in the column to calculate the mean
- We remove these columns because they do not have any valuable infromation for us

## Brain_cancer distribution visualising
- Just some basic visualisation of *brain_cancer* dataset. Just out of curiosity
- It is not that crucial and we can actually consider removing it
- 
# Question 1: How can we distinguish the most effective drugs?

## Deviding drugs in doses groups



