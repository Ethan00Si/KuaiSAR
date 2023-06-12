---
title: "KuaiSAR"
layout: default
sitemap: false
permalink: /
---

# KuaiSAR

*KuaiSAR* is a unified search and recommendation dataset containing the genuine user behavior logs collected from the short-video mobile app, [Kuaishou (快手)](https://www.kuaishou.com/en), a leading short-video app in China with over 300 million daily active users.   
**It is the first dataset which records genuine user behaviors, the occurrence of each interaction within either search or recommendation service, and the users' transitions between the two services!** 



## Overview:

As shown in the following figure, Kuaishou provides both search and recommendation services.
The figure illustrates integrated search and recommendation scenarios in Kuaishou app. 
When watching a video, the user can either scroll up and down to browse different videos with the recommendation service (from middle to left); or
tap on the magnifying glass to access the search service (from middle to right).

![kuaidata](../assets/fig/intro1.png)

From the user's perspective, the boundary between search and recommendation services may not be distinct. 
Users experience a unified service that combines both search and recommendation functionalities.
In the recommendation service, as illustrated in the figures below (a. and b.), there exist several designs that prompt users to transition into the search service. 
Similarly, in the search service, as shown in the figures below (c. and d.), various recommended queries are presented to stimulate users to engage in further searching.

![kuaidata](../assets/fig/intro2.png)


### Advantages:

Compared with other existing datasets, KuaiSAR has the following advantages:

- ✅ It is the first dataset with user genuine search and recommendation behaviors. 
- ✅ It documents the sources of users' search behaviors, such as actively typing-in searches and clicking on recommended queries.
- ✅ It comprehensively captures users' transitions between search and recommendation services, such as documenting whether users initiate a search while watching a video within the recommendation system.
- ✅ It provides abundant side information for both users and items.
- ✅ It logs users' authentic interactions, including both positive and negative feedback.

### Statistics

Basic statistics are summarized as follows:
<style>
table {
  width: 80%;
  margin-left: auto;
  margin-right: auto;
}
</style>

| Dataset | #Users | #Items | #Queries | #Actions |
|-----|-----|-----|-----|-----|
|  S-data  |  25,877   |  2,012,476   |  267,608   |   3,171,231  |
|  R-data   |  25,877   |  2,281,034   | --  |   7,493,101  |
|  Total   |   25,877  |   4,195,529  |   267,608  |  10,664,332   |

The short descriptions for each feature filed are listed as below. Please refer to this [page](./detailed_statistics.html) for more details and examples.

| **Feature**:  | Detailed Descriptions. |
|------------------------|---------------------------------------------------------------------------------------|
| **User&Item feature**:  | Users and items have abundant side information. 5 (18) features for users (items). |
| **S-action feature**:  | S-actions have 9 features, e.g., search session IDs, query keywords, and sources of entering the search service. |
| **R-action feature**:  | R-actions has 12 features, including 9 types of user feedback, e.g., likes, follows, and entering search. |
| **Social network**:    | 576 users have friends. |


## Download the data:

Work in progress.
Please wait.

## Citation

If you find it helpful, please cite our paper:
 [![LINK](https://img.shields.io/badge/-Paper%20Link-lightgrey)](https://arxiv.org/abs/not_found) [![PDF](https://img.shields.io/badge/-PDF-red)](https://arxiv.org/pdf/not_found.pdf)

```
@inproceedings{2023kuaiSAR,
  title = {KuaiSAR: A Unified Search And Recommendation Dataset} ,
  author = {work in progress},
  url = {https://doi.org/10.1145/work in progress},
  doi = {work in progress},
  year = {2023},
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

