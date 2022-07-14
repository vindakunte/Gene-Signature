# Automation of Gene Signature Generation
Gene expression signatures are very useful in understanding underlying molecular causes of disease, effects of drugs, etc. Manual extraction of collections of gene expression signatures
from GEO has been demonstrated to be highly useful.It was applied for drug repurposing, suggesting novel drugs for many diseases, and explaining mechanisms of action for many 
approved drugs. Several efforts have attempted to further annotate datasets from GEO manually; one example is Gene Expression data Mining Toward Relevant Network Discovery (GEM-TREND). 
The disadvantage of manual curation is that it does not scale up to cover the thousands of studies currently available. For similar challenges, crowdsourcing projects have been 
developed as a potential solution to overcome this obstacle.

Therefore, we need to automate this step of generating gene signatures. One way would be to classify samples in a dataset as being control or perturbation. Control in an 
experiment is a way to know that our experiment has worked for sure, for example, if we are treating something with a drug then control for that would be treated with water or 
DMSO and perturbation would be sample treated with that drug.

The target variables for classification are columns ctrl and pert which we have to correctly classify. Each row contains text which can be used for classifying it as a control 
or perturbation. The data is divided into multiple csv files, each csv file is a dataset containing samples. There are in total 20000 samples whose metadata is given, actual 
manual curated labels are given for 600 out of 20000. Now why is that, why not give labels for all the datasets, this is because we want to stress the fact that data is more 
important in situations where data is limited and it is costly to get data curated (example, chest x-ray), that's the fundamental thesis of data-centric AI.

