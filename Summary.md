# Cleaning

## Selecting brain cancer specific cell lines in all data sets
- Find out in *prism.cl* what are the names of the brain cancer cell lines and save them as a vector *names*
- Using this new vector we select the brain cancer cell lines from other dataframes and save them as new ones. For example *prism.cnv* would become *brain_cancer_cnv*

## NA removal from brain_cancer_achilles
- Achilles dataset contains information about gene KO. However some of the brain cancer cell lines do not have information about KO at all. In other words in *brain_cancer_achilles* some cell lines have entire row of NAs
- We remove such cell lines 
- before: 34 cell lines; after removal: 25 cell lines

## NA for mean substituition in brain_cancer
- In this dataset columns represent drugs in different assays and concentrations, basically column = experiment on every cell line
- There are many NAs in columns (no information how did the experiment go for some cell lines)
- We cannot remove the entire columns because we would lose a lot of information, so we substitute all the NAs for the mean of the column
- However, there are a few columns left that only have NAs. So the substitution for mean did not work there, since there are not any values in the column to calculate the mean
- We remove these columns because they do not have any valuable infromation for us

## Brain_cancer distribution visualising
- Just some basic visualisation of *brain_cancer* dataset. Just out of curiosity
- It is not that crucial and we can actually consider removing it
- it is visualized that the efficiency values are not normally distributed
- The mean of the distribution of means is -0.27

# Question 1: How can we distinguish the most effective drugs?

## Deviding drugs in doses groups
- We identify 8 standard doses, that consatantly repeat in *brain_cancer*
- As *ddx* (x for 1,2,3,4,5,6,7,8) we save the columnnames of the drugs that correspond to each dose
- After that we creat *dx* (x for 1,2,3,4,5,6,7,8) dataframe for each dose
- We identify the doses that do not exactly match the standard doses and save them in *deviation* dataframe. This dataframe originates from *brain_cancer*. Here the names of unmatched drugs are the colnames. We will need it to select the doses of these drugs
- We use *deviation* dataframe to create a second dataframe with non-standart drugs and call it *questionable drugs*. This dataframe originates from *prism.treat* and has drug names as rownames. We do this in order to see which are the doses of these drugs easier (second column of the dataframe *questionable_drugs*). These are 1144 from 11168 so around 10%.
- Now we know exactly the names of non-standard drugs and in which dose they were applied. We will work in detail on these drugs in the next chunk

## Working on drugs that do not fit the standard doses
- For now we decide that we only wanna keep the drugs that deviate from the standard doses. The chosen max deviation is 10%
- As *keep_dx* (x for 1,2,3,4,5,6,7,8) we assign drugs that have the deviation less or equal to 10%. We use the infromation from the second column of *questionable_drugs* dataframe to compare the doses to the 10% deviation (with *which* function). *keep_dx* is a vector which represents the rownumbers of drugs that satisfy the 10% max deviation
- We create *dx_extra* dataframe. Here from *brain_cancer* dataset we select only the columns that have the same name as rownames of  *keep_dx* in *questionable_drugs*
- With *cbind* function we fuse 2 dataframes: *dx* + *dx_extra*
- As a result we have selected the least deviating drugs. However there are some drugs that did not meet this requirement and have to high deviation. We save those drugs as *dose_outliers* dataframe

## Selecting relevant drugs

- Our goal here is to remove *dose_outliers* from *brain_cancer* dataframe
- We save the names of the drugs we do not want to keep in a *no_keep_drugs*
- Basically in the next to code operations we remove these drugs from *brain_cancer*. If somebody wants to know a more detailed let me know and i will explain it. I will not write it here because it would be too long and confusing

## Filter effective drugs in each dose group

- Here we create a new function called *effective_drugs*. How it works: 
  - There is one input variable **x**
  - Let's imagine our input variable is **d1**
  - The function would only select the columns from *d1* dataframe that would have mean of the column lower or equal to 0.3
- We repeat the process for all the doses and save the results in new dataframes: *effective_dx*
- At the end we make sure that the none of the drugs is in two differetn subgroups. Again if somebody wants specific details on it let me know

# Question 2: What are the targets of the effective drugs?

## Apllying the dosis separation of dataset brain_cancer on prism.treat

- Basically what we do here is to apply the division of drugs in doses on *prism.treat* dataset
- Now we have it also seperate in little dataframes, *dtx*

# Question 3: Are there any genetic markers that are specific for brain cancer subtypes?

## Dividing cell lines into subgroups

- From the column *DepMap_ID* (contains the names of the cell lines), using *grep* funtion, we divide the cell lines in 4 different subtypes
- We apply *grep* on the *disease_subtype* colun in *brain_cancer_cl* dataframe
- At the end we make sure that we have selected all 34 cell lines

# Question 4: What other factors contribute to drug effectiveness prediction?
