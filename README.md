# galactivitycalssifier
Random Forest mid-IR-optical broad-band galaxy activity classifier

Repository for galaxy actiivity clasifier from the paper "A versatile classification tool for galactic activity using optical and infrared colors"\
Astronomy & Astrophysics, accepted\
ArXiv:

**Authors:**\
Charalampos Daoutis, Elias Kyritsis, Konstantinos Kouroumpatzakis, and Andreas Zezas

### Abstract 
**Context.** The overwhelming majority of diagnostic tools for galactic activity are focused mainly on the classes of active galaxies.
Passive or dormant galaxies are often excluded from these diagnostics since they usually employ emission line features (e.g., forbidden
emission lines). Thus, most of them focus on specific types of activity or only on one activity class (e.g., active galactic nuclei or AGN). \
**Aims.** In this work, we use infrared and optical colors in order to build an all-inclusive galactic activity diagnostic tool that can
discriminate between star-forming, AGN, LINER, composite, and passive galaxies. \
**Methods.** We use the random forest algorithm in order to define a new activity diagnostic tool. As ground truth for the training of the 
algorithm, we consider galaxies that have been classified based on their optical spectra or optical colors. The potential discriminating
features that are explored for this work are 4 colors: 2 infrared and 2 optical.We explore classification criteria based on infrared colors
from the first 3 WISE bands (Bands 1, 2, and 3) supplemented with optical colors from the u, g, and r SDSS bands. From these we
seek the combination with the minimum number of colors that provides optimal results. Furthermore, to mitigate biases related to
aperture effects, we introduce a new WISE photometric scheme combing different sized apertures. \
**Results.** We develop a diagnostic tool using machine learning methods that accommodate both active and passive galaxies under
one unified classification scheme using just 3 colors. We find that the combination of W1-W2, W2-W3, and g-r colors offers good
performance while the broad availability of these colors for a large number of galaxies ensures wide applicability on large galaxy
samples. The overall accuracy is ∼81% while the achieved completeness for each class is ∼81% for star-forming, ∼56% for AGN,
∼68% for LINER, ∼65% for composite, and ∼85% for passive galaxies. \
**Conclusions.** Besides the fact that our diagnostic tool can discriminate between active and passive galaxies, it also provides a significant
improvement in the identification of AGN galaxies over the existing infrared selection methods, especially for low-luminosity
objects. This is a result of the inclusion of the optical color which also helps to identify cases of starbursts with extreme mid-IR colors
which mimic obscured AGN galaxies, a well-known problem for most IR diagnostics.

### Application of the model
This repository contains all the needed jupyter notebooks and the pre-trained random forest model for the implementations of algorithm presented in this paper. We provide a test sample *NAME* to test that your code works correctly. When you want activity classifications for your own dataset of galaxies change this file. The supported formats for your dataset is eihter 'fits' or 'csv'. The programming language used is Python3. 
- **Outout of RF model**\
After the succesful application of the model to a dataset of galaxies, a column named 'Classification' contains the label of the activity class of each galaxy in the provided catalog. For convinience we code the classification output using numbers for each activity class. Along with the classification labels we also provide the RF-predicted probabilities for every object to belong to each activity class. Below we provide a legend with the meaning of the classification output. \
**Classification legend** \
0 - star forming \
1 - AGN \
2 - LINER \
3 - composite \
4 - passive 
