# KuaiSAR

*KuaiSAR* is a unified search and recommendation dataset containing the genuine user behavior logs collected from the short-video mobile app, [Kuaishou (快手)](https://www.kuaishou.com/en), a leading short-video app in China with over 300 million daily active users.  
**It is the first dataset which records genuine user behaviors, the occurrence of each interaction within either search or recommendation service, and the users' transitions between the two services!** 


## Overview:

As shown in the following figure, Kuaishou provides both search and recommendation services.
The figure illustrates integrated search and recommendation scenarios in Kuaishou app. 
When watching a video, the user can either scroll up and down to browse different videos with the recommendation service (from middle to left); or
tap on the magnifying glass to access the search service (from middle to right).


![kuaidata](./assets/fig/intro1.png)

## Download the data:

KuaiSAR has been shared at [https://zenodo.org/](https://zenodo.org/record/8031220).

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.8031220.svg)](https://doi.org/10.5281/zenodo.8031220)

OPTION 1. Download via your browser:

You can download the dataset from this [link](https://zenodo.org/record/8031220).

OPTION 2: Download via the 'wget' command tool:

```bash
wget https://zenodo.org/record/8031220/files/KuaiSAR.zip

unzip KuaiSAR.zip
```

## Citation

If you find it helpful, please cite our paper:
 [![LINK](https://img.shields.io/badge/-Paper%20Link-lightgrey)](https://arxiv.org/abs/not_found) [![PDF](https://img.shields.io/badge/-PDF-red)](https://arxiv.org/pdf/not_found.pdf)

```
@article{Sun2023KuaiSAR,
  title={KuaiSAR: A Unified Search And Recommendation Dataset},
  author={Zhongxiang Sun and Zihua Si and Xiaoxue Zang and Dewei Leng and Yanan Niu and Yang Song and Xiao Zhang and Jun Xu},
  journal={ArXiv},
  year={2023},
  volume={abs/2306.07705}
}
```

## License

[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg


