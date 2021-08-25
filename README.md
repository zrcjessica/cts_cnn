# Chromatin Accessibility Prediction for ATAC-Seq Data with CNN
## Required Packages 
Numpy, PyTorch, Sklearn, Scipy, random, seaborn, matplotlib, Math, os
## Binary Classification
### Individual Cell Type
Prediction for each cell type spearately
#### Data
Processed count data w/ 0~50 cut
> /iblm/netapp/home/sherryh/rats/50cut

Or generated from
> /iblm/netapp/home/jezhou/make_cnn_training_data/out/pseudobulk

#### Training/Testing
> single_cell_binary.ipynb

Note: <br>
Ignore **Data Encoding Type 1** and **Trainer for Continuous Data** and run all other cells. <br>
There are six available models, but using **CNN Naive Model** would be sufficient.

### Jointly for Eight Cell Type
Prediction for cell types together, including Endothelial, Astrocytes, OPC, InhNeuron, ExNeuron, Microglia, Oligodendrocytes, Sst+.

#### Data
Merged count data w/ 25~50cut
> /iblm/netapp/home/sherryh/binary_data/50cut
> 
> /iblm/netapp/home/sherryh/binary_data/25cut

Generated from MACS2
> /iblm/netapp/home/sherryh/binary_data/MACS2

#### Training/Testing
> Multi_cell.ipynb

Note: <br>
Run all cells and select model of choice, **CNN** works the best. 

## Quantitative Prediction
### Individual Cell Type
Prediction for each cell type spearately
#### Data
Processed count data 
> /iblm/netapp/home/sherryh/new_data/zscore/
> 
> /iblm/netapp/home/sherryh/new_data/zscore_125/
> 
> /iblm/netapp/home/sherryh/new_data/zscore_500/

Or generated from
> /iblm/netapp/home/jezhou/make_cnn_training_data/out/pseudobulk

#### Training/Testing
> single_cell_continuous.ipynb

Note: <br>
There are seven available models, but only **CNN** is constructed to handle different datasets. Need to manually change feed forward layer size for other models.<br>

### Jointly for Eight Cell Type
Prediction for cell types together, including Endothelial, Astrocytes, OPC, InhNeuron, ExNeuron, Microglia, Oligodendrocytes, Sst+.

#### Data
> /iblm/netapp/home/sherryh/new_data/zscore/merged_80000_rand.npz

#### Training/Testing
> multi_quant.ipynb

Note: <br>
Not recommend for quantitative prediction as it yields much worse results than training inidividually

## Expression Prediction
### Individual Cell Type
Prediction for each cell type spearately
#### Data
Single Cell Data
> /iblm/netapp/home/sherryh/expression/full_dataset
GTEX data
> /iblm/netapp/home/sherryh/expression/gtex
