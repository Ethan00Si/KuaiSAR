---
title: "KuaiSAR"
layout: default
sitemap: false
permalink: /detailed_statistics.html
---

[HOMEPAGE](./)

## Data Descriptions:

File organization:

```bash
  KuaiSR
  ├── rec_inter.csv          
  ├── src_inter.csv
  ├── social_network.csv
  ├── user_features.csv
  └── item_features.csv
```


#### 1. Descriptions of the fields in rec_inter.csv


| Field Name           | Description                                                  | Type      | Example       |
| -------------------- | ------------------------------------------------------------ | --------- | ------------- |
| user_id              | The ID of the user.                                          | int64     | 1             |
| item_id              | The ID of the viewed item.                                   | int64     | 1             |
| playing_time         | Time of item viewing of this interaction (millisecond).      | float64   | 60792.0       |
| duration_ms          | Time of this item (millisecond).                             | float64   | 45400.0       |
| time                 | Human-readable date for this interaction (China,  Beijing time zone) | timestamp | 2023-05-22 15:53:20 |
| timestamp            | Unix timestamp (millisecond).                                | float64   | 1.684742e+12  |
| click                | Whether the user clicks the item.                            | int64     | 1             |
| forward              | Whether the user forwards the item.                          | int64     | 1             |
| like                 | Whether the user likes the item.                             | int64     | 1             |
| follow               | Whether the user follows the author of from the item.        | int64     | 1             |
| search               | Whether the user searches while watching the item.           | int64     | 1             |
| search_item_related  | Whether the user has searched for content related to the item.| int64     | 1             |


#### 2. Descriptions of the fields in src_inter.csv

| Field Name             | Description                                                               | Type      | Example          |
| ---------------------- | ------------------------------------------------------------------------- | --------- | ---------------- |
| user_id                | The ID of the user.                                                       | int64     | 14358            |
| search_session_id      | The ID of each search session.                                            | int64     | 1                |
| search_session_time    | Human-readable date for this search session (China, Beijing time zone).   | float64   | 2023-05-22 21:58:52 |
| search_session_timestamp | Unix timestamp (millisecond).                                            | float64   | 1684763932919    |
| keyword                | The keyword of the search session after anonymization.                    | list      | [20, 34, 3]      |
| search_source          | Search source of the search session                                       | string    | USER_INPUT       |
| item_id                | The item ID shown to the user in the search session.                      | int64     | 103656000000     |
| click_cnt              | Whether user click the shown item.                                        | int64     | 1                |
| item_type              | Item type of the shown item ("VIDEO", 'USER', 'IMAGE_ATLAS', 'LIVE', 'COMMODITY', 'MUSIC', 'ADVERT'). | string | VIDEO           |



#### 3. Descriptions of the fields in social_network.csv

| Field Name      | Description                                       | Type  | Example     |
| --------------- | ------------------------------------------------- | ----- | ----------- |
| user_id         | The ID of the user.                               | int64 | 19270 |
| user_follow_id  | ID of the user followed by the current user.      | int64 | 19270 |



#### 4. Descriptions of the fields in user_features.csv


| Field Name         | Description                               | Type  | Example |
| ------------------ | ----------------------------------------- | ----- | ------- |
| user_id            | The ID of the user.                       | int64 | 6302 |
| search_active_level| Search activity level of the user.          | int64 | 1       |
| rec_active_level| Recommendation activity level of the user.          | int64 | 1       |
| onehot_feat1       | An encrypted feature. Range: {0, 1, 2}    | int64 | 1       |
| onehot_feat2       | An encrypted feature. Range: {0, 1, …, 7} | int64 | 3       |



#### 5. Descriptions of the fields in item_features.csv

| Field Name                   | Description                                                      | Type      | Example     |
| ---------------------------- | ---------------------------------------------------------------- | --------- | ----------- |
| item_id                      | The ID of the item.                                              | int64     | 1           |
| caption                      | The caption of the item after anonymization.                     | list      | [1, 213, 24]|
| author_id                    | The ID of the author (0 is padding).                                             | int64     | 10          |
| item_type                    | The type of the item.                                            | string    | NORMAL      |
| upload_time                  | The upload datetime of the item (human readable: China,  Beijing time zone, 1970-1-1 is padding). | timestamp | 2023-04-22  |
| upload_type                  | Type of item uploaded.                                           | string    | LongImport  |
| first_level_category_id      | ID of the first level category for the item                      | int64     | 9           |
| first_level_category_name    | Name of the first level category for the item                    | string    | 搞笑         |
| first_level_category_name_en | English name of the first level category for the item            | string    | Funny       |
| second_level_category_id     | ID of the first second category for the item                     | int64     | 136         |
| second_level_category_name   | Name of the second level category for the item                   | string    | 搞笑段子      |
| second_level_category_name_en| English name of the second level category for the item           | string    | Funny joke  |
| third_level_category_id      | ID of the third level category for the item                      | int64     | 0           |
| third_level_category_name    | Name of the third level category for the item                    | string    | 空           |
| third_level_category_name_en | English name of the third level category for the item            | string    | empty       |
| fourth_level_category_id     | ID of the fourth level category for the item                     | int64     | 0           |
| fourth_level_category_name   | Name of the fourth level category for the item                   | string    | 空           |
| fourth_level_category_name_en| English name of the fourth level category for the item           | string    | empty       |



