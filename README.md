# NMDS_shiny
App for fast NMDS plots of sample sites

**Two excel** files/sheets are necessary:

1. **OTU table** with values in percents. The first column contains OTU label, other columns contanin abundance values in separate samples. After upload of the file, call the correct sheet by its name. 

| OTU_label | sample1 |sample2 | sample3 | 
|:---------:|:-------:|:------:|:-------:| 
|    CL01     |  1.5     |    5.4  |    10.5  | 
|  CL02   |  2.3    |   4.6  |   9.2   | 
|    CL03     |   4.5    |  4.9   |     1.1   | 


2. **Sample list** with sample names (same names as in OTU table) and further environmental variables which is used for grouping in NMDS and `envfit` function. Again, choose sheet by its name.

| sample_name | age_class |sampled_org | year | 
|:---------:|:-------:|:------:|:-------:| 
|    sample1     |  1     |    fagus  |    2015  | 
|  sample2   |  2   |   fagus  | 2014     | 
|    sample3     |   1    |  picea   |     2015   | 

---

Workflow:

1. After upload of the tables (.xlsx) it is necessary to choose the correct excel sheet by its name.

2. It is possible to filter OTUs for NMDS construction by abundance treshold in certain number of samples.

3. Colours of points in NMDS

i) For colour coding of different groups of samples choose appropriate grouping factor (i.e. column with environmental variable in the sample list) and check "Factor".

or

ii) For gradient colour of sample sites according to environmental metadata choose "Values".

4. Label points by sample ID or sample type or by other variable

5. [Hellinger transformation](http://mb3is.megx.net/gustame/reference/dissimilarity) as optional approach for lowering influence of rare OTUs.

6. By selecting columns from your sample list, you can fit several environmental variables into NMDS using `envfit` function. **No missing values in environmental variables**

7. It is possible to download .csv tables with NMDS values of each sample site for your own analysis as well as scores for environmental factors.

+ Memory on the shinyapps.io is limited, if server disconnects after upload try to reduce excel file size by deleting of unnecessary OTUs (singletons and rare ones).
 
