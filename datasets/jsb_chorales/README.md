# Bộ dữ liệu Johann Sebastian Bach (JSB) Chorales

## Nguồn dữ liệu
This dataset contains 382 chorales by Johann Sebastian Bach (in the public domain), where each chorale 
is composed of 100 to 640 chords with a temporal resolution of 1/16th. Each chord is composed of 4 integers, 
each indicating the index of a note on a piano, except for the value 0 which means "no note played".

This dataset is based on [czhuang's JSB-Chorales-dataset](https://github.com/czhuang/JSB-Chorales-dataset/) 
(`Jsb16thSeparated.npz`) which used the train, validation, test split from Boulanger-Lewandowski (2012).

Motivation: I thought it would be nice to have a version of this dataset in CSV format.

## Thông tin Tham khả
Boulanger-Lewandowski, N., Vincent, P., & Bengio, Y. (2012). Modeling Temporal Dependencies in 
High-Dimensional Sequences: Application to Polyphonic Music Generation and Transcription. 
Proceedings of the 29th International Conference on Machine Learning (ICML-12), 1159–1166.

## Sử dụng
Tải tệp tin `jsb_chorales.tgz` và giải nén nó:

```bash
$ tar xvzf jsb_chorales.tgz
```

## Cấu trúc Dữ liệu
Dữ liệu được chia thành ba thư mục (train, valid, test), với 382 tệp tin CSV: 

```
$ tree
.
├── train
│   ├── chorale_000.csv
│   ├── chorale_001.csv
│   ├── chorale_002.csv
│   │   ...
│   ├── chorale_227.csv
│   └── chorale_228.csv
├── valid
│   ├── chorale_229.csv
│   ├── chorale_230.csv
│   ├── chorale_231.csv
│   │   ...
│   ├── chorale_303.csv
│   └── chorale_304.csv
└── test
    ├── chorale_305.csv
    ├── chorale_306.csv
    ├── chorale_307.csv
    │   ...
    ├── chorale_380.csv
    └── chorale_381.csv
```

## Dữ liệu Mẫu

```
$ head train/chorale_000.csv
note0,note1,note2,note3
74,70,65,58
74,70,65,58
74,70,65,58
74,70,65,58
75,70,58,55
75,70,58,55
75,70,60,55
75,70,60,55
77,69,62,50
```
