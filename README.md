# 자연어 처리 Kaggle Competition

## Korean Hate Speech Detection
https://www.kaggle.com/competitions/korean-hate-speech-detection/overview


# 대회 소개

- 한국어 혐오 표현 감지
- 한국어 연예(entertainment) 뉴스 댓글에서의 혐오 표현 식별

## 개요 (Description)

- 연예인의 비극적인 사건 등 온라인 익명성으로 인한 부정적인 영향
- 한국 온라인 연예 뉴스 기사 9천 4백여개의 댓글 한국어 코퍼스
- 각 댓글 라벨링: 사회적 편견(social bias)의 존재 / 증오 표현 (hate speech)

## 평가 (Evaluation)

### 목표 (Goal)

- 예측 모델 개발 (hate, offensive, or none) (혐오, 공격적인 발언, 없음)

### 메트릭 (Metric)

- Macro F1-Score (정보 검색에 일반적으로 사용)
- F1-Metric: 재현율과 정밀도를 동등하게 가중치 적용


### 제출 파일 형식 (Submission File Format)

- 975개 항목과 헤더 포함된 .csv 파일 제출
- 헤더 포함: 0 - none, 1 - offensive, 2 - hate 형식 (라벨링)

# 데이터 셋

## 개요 (Description)

- 한국어 연예(entertainment) 뉴스 댓글에서의 혐오 표현 식별
- `train.hate.csv` , `dev.hate.csv` : 각 댓글에 혐오표현 라벨링 完
- `test.hate.no_label.csv` 의 모델 훈련 및 라벨링 예측
- 원본 데이터: `{train, dev, test}.news_title.txt`

## File

- `train.hate.csv`: the training set (훈련 데이터셋)
- `dev.hate.csv`: the validation set (검증 데이터셋)
- `test.hate.no_label.csv`: the test set (w/o label) (테스트 데이터 셋 (라벨링 없음) → 목표!
- `train.news_title.txt`: article titles of comments in the training set (훈련데이터셋의 댓글 기사 제목)
- `dev.news_title.txt`: article titles of comments in the validation set (검증데이터셋의 댓글 기사 제목)
- `test.news_title.txt`: article titles of comments in the test set (테스트데이터셋의 댓글 기사 제목)
- `unlabeled_comments.txt`: comments without the label (라벨링 없는 댓글)
- `unlabeled_comments.news_title.txt`: article titles of comments without the label (라벨링 없는 댓글 기사 제목)

## 데이터 구성 (Fields)

- `comments` (`str`) : news comments
- `label` (`str`) : hate label
    - `none`, `offensive`, `hate`

## 인용 (Citation)

@misc{korean-hate-speech-detection,
author = {KoreanHateSpeech},
title = {Korean Hate Speech Detection},
publisher = {Kaggle},
year = {2020},
url = {https://kaggle.com/competitions/korean-hate-speech-detection}
}






## Natural Language Processing with Disaster Tweets
https://www.kaggle.com/competitions/nlp-getting-started/overview


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