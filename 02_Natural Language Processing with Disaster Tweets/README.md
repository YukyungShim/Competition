# 대회 소개

- 재난 트윗(Disaster Tweets)과 자연어 처리 (Natural Language Processing)
- 진짜 재난 트윗인지 아닌지 예측하기

## 개요 (Description)

- 트위터는 비상 시 중요한 커뮤니케이션 플랫폼
- ex. 시각적 사진 + “ABLAZE (불타는)” 단어 표현
- 어떤 트윗이 실제 재난에 대한 것인지, 아닌지 예측하는 머신러닝 구축 목표
- 수동으로 분류된 10,000개의 트윗 데이트 세트

## 평가 (Evaluation)

- predicted & expected answer의 F1 score로 평가

## 제출 파일 형식 (Submission File Format)

- test 셋에 있는 각각의 ID에 대해 1 (재난 o), 0 (재난 x)
- 헤더 포함 (id, target)

# 데이터 셋

## 개요 (Description)

- The `text` of a tweet
- A `keyword` from that tweet (although this may be blank!) (빈칸 포함)
- The `location` the tweet was sent from (may also be blank) (빈칸 포함)

## 목표 (Predicting)

- 진짜 재난인지 아닌지 주어진 트윗 구분 예측
- 1 - predict (재난 o), 2 - not (재난 x)

## File

- **train.csv** - the training set (훈련 데이터 셋)
- **test.csv** - the test set (테스트 데이터 셋)
- **sample_submission.csv** - a sample submission file in the correct format (올바른 형식의 제출 파일 예시)

## 데이터 구성 (Columns)

- `id` - a unique identifier for each tweet
- `text` - the text of the tweet
- `location` - the location the tweet was sent from (may be blank)
- `keyword` - a particular keyword from the tweet (may be blank)
- `target` - in **train.csv** only, this denotes whether a tweet is about a real disaster (`1`) or not (`0`)

## 인용 (Citation)

@misc{nlp-getting-started,
author = {Addison Howard, devrishi, Phil Culliton, Yufeng Guo},
title = {Natural Language Processing with Disaster Tweets},
publisher = {Kaggle},
year = {2019},
url = {https://kaggle.com/competitions/nlp-getting-started}
}