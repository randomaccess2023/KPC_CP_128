# Feature Extraction and Unsupervised Clustering of Histopathological Images of Pancreatic Cancer Using Information Maximization

This repository shows the code implementation and figures for the conference paper titled _**Feature Extraction and Unsupervised Clustering of Histopathological Images of Pancreatic Cancer Using Information Maximization**_.

Let's walk through this repository:

- **kpc16** folder:
1. `part_1_5000e_16c_training.ipynb`: This file has the code for training the unsupervised model using the 16-cluster set.
2. `part_2_5000e_16c_clustering.ipynb`: This file offers the code for clustering the training images using the trained unsupervised model with the 16-cluster set. We only showed the samples using the _HE staining_ due to the page limitations during the paper submission.
3. `part_3_5000e_16c_umap.ipynb`: This file shows the code for plotting _UMAP_ for the 16-cluster set.
4. `part_4_5000e_16c_NLL.ipynb`: This file includes the source code to compute the nagative log-likelihood for the 16-cluster set.
5. `part_5_save_clusters.ipynb`: This file contains the code for saving clusters individually for the 16-cluster set.

`HHH16 & C16 & D16.csv` file has the information regarding the latent space.

> **kpc16** folder has two subfolders: _**clus16**_ and _**models16**_.
>> _**clus16**_ has the individual clusters in the form of `.csv` files. We obtained these files after executing the code shown in `part_5_save_clusters.ipynb` script.
>>> _**models16**_ has 3 `.ckpt` files: `model_en_202203211747_5000.ckpt`, `model_cl_202203211747_5000.ckpt`, and `model_de_202203211747_5000.ckpt`. These three files form our unsupervised model. `hist_modelS_202203211747_5000.tsv` file stores diiferent metrics obtained during the training of our model.

#### The files present in the _kpc16_ folder can also be obtained for cluster sets of 8, 12, and 20. We haven't shown them here to avoid repetitiveness. In the paper, we showed the _`UMAP`_ and _`clustering`_ results for 8-cluster set. These can be obtained after training the model using `part_1_5000e_8c_training.ipynb` file for the 8-cluster set. After that, running `part_2_5000e_8c_clustering.ipynb` and `part_3_5000e_8c_umap.ipynb` will provide the desired results. The users will have to do these by themselves.

`optimum_NLL.ipynb` file plots a line graph utilizing the negative log-likelihoods for the chosen cluster sets (8, 12, 16, and 20).

> Finally, The folder `Figures` has 5 `.png` files in it: _Fig_1.png_, _Fig_2.png_, _Fig_3.png_, _Fig_4.png_, and _Fig_5.png_. These are the same figures that can be seen in the conference paper.

## This repository uses `MIT License`. Read the terms and conditions from _LICENSE_ text file.

# Read the paper from here: [KPC_CP](https://ieeexplore.ieee.org/document/10014057)
