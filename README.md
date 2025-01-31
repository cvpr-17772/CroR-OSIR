# CroR-OSIR: Cross-Rejective Open-Set SAR Image Registration
# Introduction
This GitHub project is for the rebuttal of CVPR-17772. Due to space limitations, we have uploaded some additional experimental visualization results here. Thank you for your careful review!
# Rejection Mechanism
### Visualization On The Yama Dataset
#### The visual results without the rejection module and without post-processing.

![](Rejection%20Mechanism/Visualization%20On%20The%20Yama%20Dataset/yama_reject_ablation_without_post_and_reject.png)

As shown in the figure, the results without the rejection module and any post-processing contain incorrect matchings and a large number of redundant point pairs, which lead to a decrease in matching accuracy.
#### The visual results without the rejection module and with post-processing.

![](Rejection%20Mechanism/Visualization%20On%20The%20Yama%20Dataset/yama_reject_ablation_withpost_without_reject.png)
After applying RANSAC for post-processing, incorrect and some redundant point pairs are removed. However, remaining redundant points with insufficient matching quality limit further improvements in registration accuracy.
#### The visual results with the rejection module and without post-processing.

![](Rejection%20Mechanism/Visualization%20On%20The%20Yama%20Dataset/yama_reject_ablation_withreject_withoutpost.png)

As shown, the rejection module effectively removes incorrect matchings and redundant points, achieving better registration accuracy without post-processing.
### Visualization On The YellowR1 Dataset
#### The visual results without the rejection module and without post-processing.

![](Rejection%20Mechanism/Visualization%20On%20The%20YellowR1%20Dataset/yellowa_reject_ablation_withoutreject_withoutpost.png)

#### The visual results without the rejection module and with post-processing.

![](Rejection%20Mechanism/Visualization%20On%20The%20YellowR1%20Dataset/yellowa_reject_ablation_withoutreject_withpost.png)

#### The visual results with the rejection module and without post-processing.

![](Rejection%20Mechanism/Visualization%20On%20The%20YellowR1%20Dataset/yellowa_reject_ablation_withreject_withoutpost.png)

# Comparison Visualizations

### Visualization results On The Yama Dataset

#### SIFT

![](Comparison%20Visualizations/Visualization%20results%20On%20The%20Yama%20Dataset/CBchartYama_SIFT.png)

#### SuperPoint

![](Comparison%20Visualizations/Visualization%20results%20On%20The%20Yama%20Dataset/CBchartYama_SuperPoint.png)

#### DALF

![](Comparison%20Visualizations/Visualization%20results%20On%20The%20Yama%20Dataset/CBchartYama_DALF.png)

#### XFeat

![](Comparison%20Visualizations/Visualization%20results%20On%20The%20Yama%20Dataset/CBchartYama_XFeat.png)

#### DBMDF

![](Comparison%20Visualizations/Visualization%20results%20On%20The%20Yama%20Dataset/CBchartYama_DBMDF.png)

#### CroR-OSIR

![](Comparison%20Visualizations/Visualization%20results%20On%20The%20Yama%20Dataset/CBchartYama_CroR-OSIR.png)

### Visualization results On The YellowR1 Dataset

#### SIFT

![](Comparison%20Visualizations/Visualization%20results%20On%20The%20YellowR1%20Dataset/CBchartYellowR1_SIFT.png)

#### SuperPoint

![](Comparison%20Visualizations/Visualization%20results%20On%20The%20YellowR1%20Dataset/CBchartYellowR1_SuperPoint.png)

#### DALF

![](Comparison%20Visualizations/Visualization%20results%20On%20The%20YellowR1%20Dataset/CBchartYellowR1_DALF.png)

#### XFeat

![](Comparison%20Visualizations/Visualization%20results%20On%20The%20YellowR1%20Dataset/CBchartYellowR1_XFeat.png)

#### DBMDF

![](Comparison%20Visualizations/Visualization%20results%20On%20The%20YellowR1%20Dataset/CBchartYellowR1_DBMDF.png)

#### CroR-OSIR

![](Comparison%20Visualizations/Visualization%20results%20On%20The%20YellowR1%20Dataset/CBchartYellowR1_CroR-OSIR.png)

# Comparisons on Other Benchmarks

### DALF
![](visualation/optical_DAlF.png)
### XFeat
![](visualation/optical_XFeat.png)
### DBMDF
![](visualation/optical_DBMDF.png)
### CroR-OSIR
![](visualation/optical_CroR-OSIR.png)
<!-- # Installation
## Make Data
## SupCon Pretraining
## CroR-OSR training and the fintune of SupCon module

# Test accurancy -->
