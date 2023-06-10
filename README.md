# KuaiSAR

*KuaiSAR* is a unified search and recommendation dataset collected from the genuine user behavior logs of the short-video mobile app, [Kuaishou (快手)](https://www.kuaishou.com/en), a leading short-video app in China with over 300 million daily active users.  
**It is the first dataset which records genuine user behaviors, the occurrence of each interaction within either search or recommendation service, and the users' transitions between the two services!** 
<!-- *KuaiRand* is an unbiased sequential recommendation dataset collected from the recommendation logs of the video-sharing mobile app, [Kuaishou (快手)](https://www.kuaishou.com/cn).  **It is the first recommendation dataset with millions of  intervened interactions of randomly exposed items inserted in the standard recommendation feeds!**  -->

<!-- Another related **open-sourced** dataset is **[KuaiRec](https://kuairec.com/)**. -->


## Overview:

As shown in the following figure, Kuaishou provides both search and recommendation services.
As users scroll down the screen, they can discover new recommended short videos that they may be interested in.
When users click on the magnifying glass, they can enter the main search page and use the search engine to find videos of interest.

<!-- ![kuaidata](https://cdn.chongminggao.top/figure/KuaiRand-homepage.png) -->
![kuaidata](./assests/fig/intro1.png)

From the user's perspective, the boundary between search and recommendation services may not be distinct. Users experience a unified service that combines both search and recommendation functionalities.
In the recommendation service, there exist several designs that prompt users to transition into the search service. Similarly, in the search service, various recommended queries are presented to stimulate users to engage in further searching.

<!-- <img src="https://cdn.chongminggao.top/figure/kuaishou-app.png" alt="kuaishou-app" style="display: block;margin: auto;zoom:35%;" /> -->



### Advantages:

Compared with other existing datasets, KuaiSAR has the following advantages:

- ✅ It is the first dataset with user genuine search and recommendation behaviors. 
- ✅ It documents the sources of users' search behaviors, such as actively typing-in searches and clicking on recommended queries.
- ✅ It comprehensively captures users' transitions between search and recommendation services, such as documenting whether users initiate a search while watching a video within the recommendation system.
- ✅ It provides abundant side information for both users and items.
- ✅ It logs users' authentic interactions, including both positive and negative feedback.

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


| Field Name          | Description                                               | Type       | Example          |
| ------------------- | --------------------------------------------------------- | ---------- | ---------------- |
| user_id             | The ID of the user.                                       | int64      | 6302591          |
| video_id            | The ID of the viewed video.                               | int64      | 103656000000     |
| playing_time        | Time of video viewing of this interaction (millisecond).  | float64    | 60792.0          |
| duration_ms         | Time of this video (millisecond).                         | float64    | 45400.0          |
| time                | Human-readable date for this interaction (China,  Beijing time zone) | timestamp | 2023-05-22 15:53:20 |
| timestamp           | Unix timestamp (millisecond).                             | float64    | 1.684742e+12     |
| click               | Whether the user clicks the video.                        | int64      | 1                |
| forward             | Whether the user forwards the video.                      | int64      | 1                |
| like                | Whether the user likes the video.                         | int64      | 1                |
| follow              | Whether the user follows the author of from the video.    | int64      | 1                |
| search              | Whether the user searches while watching the video.       | int64      | 1                |
| search_video_related| Whether the user has searched for content related to the video. | int64 | 1           |

#### 2. Descriptions of the fields in src_inter.csv

| Field Name                 | Description                                               | Type       | Example          |
| -------------------------- | --------------------------------------------------------- | ---------- | ---------------- |
| user_id                    | The ID of the user.                                       | int64      | 6302591          |
| search_session_id          | The ID of each search session.                            | int64      | 200              |
| search_session_time        | Human-readable date for this search session (China, Beijing time zone). | float64 | 2023-05-22 21:58:52 |
| search_session_timestamp   | Unix timestamp (millisecond).                             | float64    | 1684763932919    |

#### 3. Descriptions of the fields in social_network.csv

| Field Name      | Description                                       | Type  | Example     |
| --------------- | ------------------------------------------------- | ----- | ----------- |
| user_id         | The ID of the user.                               | int64 | 510091130 |
| user_follow_id  | ID of the user followed by the current user.      | int64 | 918564140 |

#### 4. Descriptions of the fields in user_features.csv

| Field Name         | Description                               | Type  | Example |
| ------------------ | ----------------------------------------- | ----- | ------- |
| user_id            | The ID of the user.                       | int64 | 6302591 |
| recommendation_active_level| Recommendation active level of the user.          | int64 | 1       |
| search_active_level| Search active level of the user.          | int64 | 1       |
| onehot_feat1       | An encrypted feature. Range: {0, 1, 2}    | int64 | 1       |
| onehot_feat2       | An encrypted feature. Range: {0, 1, …, 7} | int64 | 3       |

#### 5. Descriptions of the fields in video_features.csv


| Field Name                          | Description                                                  | Type       | Example          |
| ----------------------------------- | ------------------------------------------------------------ | ---------- | ---------------- |
| video_id                            | The ID of the video.                                         | int64      | 103656000000     |
| caption                             | The caption of the video after anonymization.                | list       | [1, 213, 24]     |
| author id                           | The ID of the author.                                        | int64      | 875927800        |
| video_type                          | The type of the video.                                       | string     | NORMAL           |
| upload_time                         | The upload datetime of the video (human readable: China,  Beijing time zone). | timestamp | 2023-04-22 15:53:20 |
| upload_timestamp                    | Unix timestamp (millisecond).                                | float64    | 1682150000000    |
| upload_type                         | Type of video uploaded.                                      | string     | LongImport       |
| topic_tag                           | Topic of the video.                                          | list       | ["Gif快手"]      |
| first_level_category_id             | ID of the first level category for the video                 | int64      |                  |
| first_level_category_name           | Name of the first level category for the video               | string     |                  |
| first_level_category_name_English   | English name of the first level category for the video       | string     |                  |
| second_level_category_id            | ID of the first second category for the video                | int64      |                  |
| second_level_category_name          | Name of the second level category for the video              | string     |                  |
| second_level_category_name_English  | English name of the second level category for the video      | string     |                  |
| third_level_category_id             | ID of the third level category for the video                 | int64      |                  |
| third_level_category_name           | Name of the third level category for the video               | string     |                  |
| third_level_category_name_English   | English name of the third level category for the video       | string     |                  |
| fourth_level_category_id            | ID of the fourth level category for the video                | int64      | 3                |
| fourth_level_category_name          | Name of the fourth level category for the video              | string     |                  |
| fourth_level_category_name_English  | English name of the fourth level category for the video      | string     |                  |


#### 6. Descriptions of the fields in search_features.csv

| Field Name         | Description                                                         | Type  | Example      |
| ------------------ | ------------------------------------------------------------------- | ----- | ------------ |
| search_session_id  | The ID of the search session.                                       | int64 | 200          |
| keyword            | The keyword of the search session after anonymization.              | list  | [20, 34, 3]  |
| search_source      | Search source of the search session                                 | string| USER_INPUT   |
| item_id            | The item ID shown to the user in the search session.                | int64 | 103656000000 |
| click_cnt          | Whether user click the shown item.                                  | int64 | 1            |
| item_type          | Item type of the shown item ("VIDEO", 'USER', 'IMAGE_ATLAS', 'LIVE', 'COMMODITY', 'MUSIC', 'ADVERT'). | string| VIDEO        |


