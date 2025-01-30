# CroR-OSIR: Cross-Rejective Open-Set SAR Image Registration
# Introduction
This github project is the code for the paper 《Cross-Rejective Open-Set SAR Image Registration》, which uses Open Set recognition to solve the problem of redundant point pairs in image registration, so we'll show you a visualization and update the code to keep the project up to date！
# Visualization Results
## Visualization of the effect of the rejection module

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

## Visualization results of the compared methods and our methods

### Visualization results On The Yama Dataset

### Visualization results On The YellowR1 Dataset

# Installation
## Make Data
## SupCon Pretraining
## CroR-OSR training and the fintune of SupCon module

# Test accurancy
