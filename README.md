# ACDC-Kaggle-challenge

We perfromed cardiac pathology prediction on the ACDC dataset (Automatic Cardiac Diagnosis Challenge). The dataset contains data from 150 multi-equipment CMRI
recordings with reference measurements, segmentation of the myocardium,
left ventricle, and right ventricle, as well as disease classification from two
medical experts. In the initial challenge, heart segmentation and patient classifications were missing for the last 50 patients. However, in this simplified
version, only the segmentation of the left ventricle was missing. As a result,
we performed left ventricle segmentation using morphological transformations
on the myocardium and border detection to segment the left ventricle, which is
located inside the myocardium. Cardiac parameters, such as ejection fraction
and ventricle volumes, were then calculated from the segmentation masks.
Furthermore, these parameters were used as features to train a random forest
and an MLP. The dataset was split into training/validation (90% for crossvalidation) and testing (10%). The most important features were extracted,
and different classifiers were trained afterwards.
