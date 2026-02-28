# msInfer


### Inferring paired large-scale single-cell proteomic for RNA by msInfer

Obtaining high-throughput, large-scale, and paired transcriptomic and proteomic data at the single-cell level is crucial for understanding the complex functions and phenotypic characteristics of multicellular organisms. However, current biomolecular measurement technologies are limited by detect only a small panel of functional proteins or by low cellular throughput, which hinders comprehensive analysis of cell function. Therefore, there is an urgent need of computational approaches to bridge the gap between the high-throughput nature of single-cell RNA sequencing (scRNA-seq) and the large-scale protein profiling offered by single-cell proteomics. We describe msInfer to leverage single-cell proteomic data as a reference to infer large-scale protein expression profiles for each cell in scRNA-seq data. msInfer includes a self-supervised contrastive learning module that aligns unpaired transcriptomic and proteomic data, and an unsupervised weight generation module that performs the inference. Through systematic evaluation from multiple dimensions, msInfer demonstrates high concordance between inferred and experimentally measured protein expression. msInfer enables effective downstream tasks such as differential protein identification and cell clustering. Moreover, it outperforms existing methods in multi-omics integration, significantly enhancing capabilities in cell subtype annotation, drug mechanism exploration, and the construction of single-cell multi-omics atlas.


<p align="center">
  <img width="80%" src="image/Workflow_github.png">
</p>



## Environment

#### Option1 [recommend]
We provide more convenient online running examples that can be executed directly through Colab, without the need for local environment setup. Click the Colab icon to directly enter the online runtime environment to run the scInfer demo. 
<a href="https://colab.research.google.com/github/YuzhiSun/scInfer_colab/blob/main/Unpaired_benchmark_breast.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

#### Option2
If you want to configure the environment locally, you can follow the configuration methods below.

The running environment of scInfer can be installed from enviornment.yml
```
> conda env create --name env_name -f environment.yml  
```

## Turorial

The following notebooks are provided to show how to run scInfer model

1. [BreastTaskEmbedding](BreastTaskEmbedding.ipynb) gives a detailed description of how to obtain embedding features for transcriptomics and proteomics.
2. [BreastTaskInfer](BreastTaskInfer.ipynb) gives a detailed description of how to infer proteomics data for transcriptomics.
3. [PancreasTaskEmbedding](PancreasTaskEmbedding.ipynb) gives a detailed description of how to generate embedding features for the target dataset by pre-training on gold standard data.
4. [PancreasTaskInfer](PancreasTaskInfer.ipynb) gives a detailed of how to infer proteomics data for target transcriptomics.

## Data

The data is stored on Zendo(https://doi.org/10.5281/zenodo.14986872); simply unzip the file named scInferData.zip into scInferData folder.

## Requirements

We can successfully run it on a single RTX 2080Ti GPU.

## Questions

If you have any suggestions/ideas for scInfer, please don't hesitate to reach out to us. You can reach us by email(yuzhi@stu.hit.edu.cn).


