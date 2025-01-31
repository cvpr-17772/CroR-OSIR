# CroR-OSIR: Cross-Rejective Open-Set SAR Image Registration
# Introduction
This GitHub project is for the details of CVPR-17772. Due to space limitations, we have uploaded some additional experimental visualization results here. Thank you for your careful review!
# Rejection Mechanism


We conducted experiments on the **Yama dataset** and **YellowR1 dataset** using the SIFT algorithm to detect keypoints. **1223** keypoints were detected in the reference image and **1374** in the sensed image. On the **YellowR1** dataset, we detected **1339** keypoints in the reference image and **1201** keypoints in the sensed image. The encoder was pre-trained for **50 epochs**, followed by training the **R-domain** and **S-domain** classification heads for an additional **50 epochs**. We removed the reject module, with **cross-domain estimation every 5 epochs**. The following registration results were based on matches approved by both branches. We present the results from the **10th cross-domain estimation**. The detailed experimental results are presented in the table below.

![](tables/reject_module.png)

### Visualization On The Yama Dataset

#### The visual results without the reject module and without post-processing.

![](Rejection%20Mechanism/Visualization%20On%20The%20Yama%20Dataset/yama_reject_ablation_without_post_and_reject.png)

As shown in the above figure, the results without the reject module and any post-processing contain a large number of **redundant point pairs**, which lead to a decrease in matching accuracy. 

Then, we performed **post-processing** to remove erroneous match pairs and visualized the results after eliminating the incorrect matches.

#### The visual results without the reject module and with post-processing.

![](Rejection%20Mechanism/Visualization%20On%20The%20Yama%20Dataset/yama_reject_ablation_withpost_without_reject.png)
After applying **RANSAC** for post-processing, incorrect and some redundant point pairs are removed. However, remaining redundant points with insufficient matching quality limit further improvements in registration accuracy.

Then, we compared this result with the one using only the reject module (with a rejection threshold of **0.95**). The results using only the rejection module are shown in the figure below.

#### The visual results with the reject module and without post-processing.

![](Rejection%20Mechanism/Visualization%20On%20The%20Yama%20Dataset/yama_reject_ablation_withreject_withoutpost.png)

As shown above, the reject module effectively removes incorrect matchings and redundant points, achieving better registration accuracy without post-processing.
### Visualization On The YellowR1 Dataset

First, we present the results without the reject module and without post-processing.

#### The visual results without the reject module and without post-processing.

![](Rejection%20Mechanism/Visualization%20On%20The%20YellowR1%20Dataset/yellowa_reject_ablation_withoutreject_withoutpost.png)

Then, we performed post-processing and present the visualized results below.

#### The visual results without the reject module and with post-processing.

![](Rejection%20Mechanism/Visualization%20On%20The%20YellowR1%20Dataset/yellowa_reject_ablation_withoutreject_withpost.png)

Then, we present the results using only the reject module (rejection threshold = **0.95**).
#### The visual results with the reject module and without post-processing.

![](Rejection%20Mechanism/Visualization%20On%20The%20YellowR1%20Dataset/yellowa_reject_ablation_withreject_withoutpost.png)

# Comparison Visualizations

To further demonstrate the accuracy difference between our method and the comparison methods, we conducted experiments on the **YellowR1** and **Yama** datasets with a rejection threshold of **0.95**. Other experimental settings are as described in Section 4.1 of the paper. We provide the registration point-line diagrams and checkerboard images generated by different algorithms. The point-line diagrams show the number and distribution of the matched points, while the chessboard images more precisely reflect the registration accuracy. The table below shows the actual accuracy on two datasets.
![](tables/compared_table.png)
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
We conducted experiments on the **"abstract"** image of the **HPatches-sequences-release** dataset. In the experiment, the **rejection threshold** is set to **0.99**, and initial keypoints are detected using **SIFT**. A total of **1451** keypoints are detected in the **reference image**, and **1489** keypoints in the **sensed image**. The remaining experimental settings were the same as described in **Section 4.1**.
The detailed experimental results are shown in the table below.
![](tables/other_benckmark.png)
### DALF
![](Comparisons%20on%20Other%20Benchmarks/DALF/optical_DAlF.png)

### XFeat
![](Comparisons%20on%20Other%20Benchmarks/XFeat/optical_XFeat.png)
### DBMDF
![](Comparisons%20on%20Other%20Benchmarks/DBMDF/optical_DBMDF.png)
### CroR-OSIR
![](Comparisons%20on%20Other%20Benchmarks/CroR-OSIR/optical_CroR-OSIR.png)
<!-- # Installation
## Make Data
## SupCon Pretraining
## CroR-OSR training and the fintune of SupCon module

# Test accurancy -->
