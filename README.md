# Chromatin Accessibility Prediction for ATAC-Seq Data with CNN
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
> /iblm/netapp/home/sherryh/new_data/data_concat_25_50/

Generated from MACS2
> /iblm/netapp/home/sherryh/new_data/new_labels/

Files: c5c2neg.npz, c6neg.npz, merge_c2_neg.npz

#### Training/Testing
> Multi_cell.ipynb
Note: <br>
Run all cells and select model of choice, **CNN** works the best. 
