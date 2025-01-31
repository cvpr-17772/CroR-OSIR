# CroR-OSIR: Cross-Rejective Open-Set SAR Image Registration
# Introduction
This GitHub project is for the rebuttal of CVPR-17772. Due to space limitations, we have uploaded some additional experimental visualization results here. Thank you for your careful review!
# Rejection mechanism
### Visualization On The Yama Dataset
#### The visual results without the rejection module and without post-processing.

![](visualation/yama_reject_ablation-2_01.png)

As shown in the figure, the results without the rejection module and any post-processing contain incorrect matchings and a large number of redundant point pairs, which lead to a decrease in matching accuracy.
#### The visual results without the rejection module and with post-processing.

![](visualation/yama_reject_ablation-2_02.png)
After applying RANSAC for post-processing, incorrect and some redundant point pairs are removed. However, remaining redundant points with insufficient matching quality limit further improvements in registration accuracy.
#### The visual results with the rejection module and without post-processing.

![](visualation/yama_reject_ablation-2_03.png)
As shown, the rejection module effectively removes incorrect matchings and redundant points, achieving better registration accuracy without post-processing.
### Visualization On The YellowR1 Dataset
#### The visual results without the rejection module and without post-processing.

![](visualation/yellowa_reject_ablation-2_01.png)

#### The visual results without the rejection module and with post-processing.

![](visualation/yellowa_reject_ablation-2_02.png)

#### The visual results with the rejection module and without post-processing.

![](visualation/yellowa_reject_ablation-2_03.png)

# Comparison Visualizations

### Visualization results On The Yama Dataset

#### SIFT

![](visualation/CBchartYama_4_01.png)

#### SuperPoint

![](visualation/CBchartYama_4_02.png)

#### DALF

![](visualation/CBchartYama_4_03.png)

#### XFeat

![](visualation/CBchartYama_4_04.png)

#### DBMDF

![](visualation/CBchartYama_4_05.png)

#### CroR-OSIR

![](visualation/CBchartYama_4_06.png)

### Visualization results On The YellowR1 Dataset

#### SIFT

![](visualation/CBchartYellowR1_4_01.png)

#### SuperPoint

![](visualation/CBchartYellowR1_4_02.png)

#### DALF

![](visualation/CBchartYellowR1_4_03.png)

#### XFeat

![](visualation/CBchartYellowR1_4_04.png)

#### DBMDF

![](visualation/CBchartYellowR1_4_05.png)

#### CroR-OSIR

![](visualation/CBchartYellowR1_4_06.png)

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
