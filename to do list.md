# 2021-topic-01-team-03

Till 24.05
- [x] Establish how big can be the deviation of non-standard doses, from the standard ones. **Teamwork Xenia & Ilya <3**
- [x] Establish the threshold for effective drugs. **Lea+Lennard**
- [x] Create another file which includes all steps that are planned or have been done concerning the questions, small summary. **Ilya**
- [x] Removing irrelevant colums/rows from datasets. **Ilya**

Till 31.05
- [x] Do we want to select just effective drugs in all 34 cell lines or we want to select effective drugs specifically for each of 4 subtypes? Somebody needs to look into it and see if it is worth it or not. **Xenia**
- [x] Solve the "Filter effective drugs" problem. **Ilya**
- [x] Select the drugs that are effective in multiple doses. **Ilya**
- [x] Select drug targets. **Ilya**
- [x] Why is the threshold 0,3 and not 0? **Lea**
- [ ] Look into how effective_in_all_doses drugs vary in their effect on cell proliferation, depending on the dose (in brain_cancer data frame). Look for trends and create groups from drugs that have similarities. **Lea**
- [x] Which cell lines miss from achilles? **Cedrik**
- [x] Find a way to justify the 0,3. **Lennard**

Till 7.06y
- [ ] **What to do with the drug targets? How to examine gene targets of the effective drugs and what to do with them? How do we work further? (prism.treat + prism.achilles + prism.cnv) As I understood Stefan meant that it tis not worth it and that the whole idea of repurpusing is that these drugs act differently and not like they are supposed it. So the effect is not attributed to the designed drug target**
- [x] Select one dose to continue working on. **Ilya**
- [ ] Determine specific drugs for each brain cancer subtype or is there any trend between cell lines and drugs. Basically: are there any drugs that are more effective for certain cells? **Cedrik**
- [x] See what is the norm is in brain_cancer_treat and brain_cancer_cnv and brain_cancer_achilles. Generate general information and visualisation of this dataframs. **Lennard**
- [x] Which TPM is considered to be an overexpression? **Lea**

Till 14.06
- [ ] **We need some kind of a test and do more clustering. How do we work with genes?**
- [ ] Wilcoxon Signed Rank Test. Who?
- [ ] Maybe somebody could make our code more structured according to Stefan's suggestions
- [ ] See if there is any specific characteristics on gene expression for the cancer subtypes. Or are there in general any tendencies between certain cell lines. -> Via Wilcoxon Test **Xenia**
- [ ] Visualization eg heatmap of the effective drugs **Cedrik**

In the pipeline:
- [ ] Try to find a way to store long codes in loops just to make it more professional (when enough time for it)
- [ ] What happens with drugs which are effective but dose dependant?


Idea how to continue:
- subdivision of drugs and gene expression -> is there a match? 
