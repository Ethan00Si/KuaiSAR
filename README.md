# KuaiSAR: A Unified Search and Recommendation Dataset

[![LICENSE](https://img.shields.io/badge/license-CC%20BY--SA%204.0-green)](https://github.com/chongminggao/KuaiRand/blob/main/LICENSE)

*KuaiSAR* is a unified search and recommendation dataset collected from the genuine user behavior logs of the short-video mobile app, [Kuaishou (快手)](https://www.kuaishou.com/en), a leading short-video app in China with over 300 million daily active users.  
**It is the first dataset which records genuine user behaviors, the occurrence of each interaction within either search or recommendation service, and the users' transitions between the two services!** 
<!-- *KuaiRand* is an unbiased sequential recommendation dataset collected from the recommendation logs of the video-sharing mobile app, [Kuaishou (快手)](https://www.kuaishou.com/cn).  **It is the first recommendation dataset with millions of  intervened interactions of randomly exposed items inserted in the standard recommendation feeds!**  -->

<!-- Another related **open-sourced** dataset is **[KuaiRec](https://kuairec.com/)**. -->


## Overview:

The following figure gives an example of the dataset. It illustrates a user interaction sequence along with the user's rich feedback signals.

<!-- ![kuaidata](https://cdn.chongminggao.top/figure/KuaiRand-homepage.png) -->

These feedback signals are collected from the two main user interfaces (UI) in Kuaishou APP shown as follows:

<!-- <img src="https://cdn.chongminggao.top/figure/kuaishou-app.png" alt="kuaishou-app" style="display: block;margin: auto;zoom:35%;" /> -->

<!-- In the random exposure stage, each recommended video in the dataset has an equal probability being replaced by a random video sampled from an item pools. About $0.37\%$ Interactions are replaced in the final results.  -->

#### Advantages:

Compared with other existing datasets, KuaiSAR has the following advantages:

- ✅ It is the first dataset with user genuine search and recommendation behaviros.
- ✅ It has all user-system interactions in search and recommendation scenarios, including interactions of both postive and negative feedback.
- ✅ It has diverse side information including explicit user IDs, interaction timestamps, and rich features for users and items.
- ✅ Each user has thousands of historical interactions on average.

If you find it helpful, please cite our paper:
 [![LINK](https://img.shields.io/badge/-Paper%20Link-lightgrey)](https://arxiv.org/abs/not_found) [![PDF](https://img.shields.io/badge/-PDF-red)](https://arxiv.org/pdf/not_found.pdf)

```
@inproceedings{2023kuaiSAR,
  title = {KuaiSAR: placeholder} ,
  author = {placeholder},
  url = {https://doi.org/10.1145/not_found},
  doi = {10.1145/not_found},
  year = {2023},
}
```

## Download the data:

Work in progress.
Please wait.

---

## Data Descriptions:

File organization:

```bash
  KuaiSR
  ├── rec_inter.csv          
  ├── src_inter.csv
  ├── social_network.csv
  ├── user_features.csv
  ├── video_features.csv
  └── search_features.csv
```

#### Statistics:
Work in progress.
Please wait.

#### 1. Descriptions of the fields in rec_inter.csv

| Field Name:	  | Description  | Type  |Example|
|---|---|---|---|
|  user_id | The ID of the user.  | int64   | 6302591 |
|  video_id |  The ID of the viewed video.   |  int64 |103656000000|
| playing_time  | Time of video viewing of this interaction (millisecond).  | float64  | 60792.0  |
|duration_ms| Time of this video (millisecond).  |float64   |  45400.0 |


#### 2. Descriptions of the fields in src_inter.csv

#### 3. Descriptions of the fields in social_network.csv

#### 4. Descriptions of the fields in user_features.csv

#### 5. Descriptions of the fields in video_features.csv

#### 6. Descriptions of the fields in search_features.csv




