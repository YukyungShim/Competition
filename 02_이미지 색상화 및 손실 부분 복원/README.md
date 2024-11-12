## 2. 이미지 색상화 및 손실 부분 복원 AI 경진대회
알고리즘 | 비전 | 이미지 복원 | 이미지 색상화 | SSIM

https://dacon.io/competitions/official/236420/data

# 대회 소개
- 이미지의 색상화와 손실 부분을 복원하는 AI 알고리즘 개발
- 손실된 이미지의 결손 부분을 복구하고, 흑백 이미지에 자연스러운 색을 입히는 AI 알고리즘 개발

# 데이터 셋
## 훈련 데이터 셋
- train_input [폴더] : 흑백, 일부 손상된 PNG 학습 이미지 (input, 29603장)-
- train_gt [폴더] : 원본 PNG 이미지 (target, 29603장)
- train.csv [파일] : 학습을 위한 Pair한 PNG 이미지들의 경로

## 테스트 데이터 셋
- test_input [폴더] : 흑백, 일부 손상된 PNG 평가 이미지 (input, 100장)
- test.csv [파일] : 추론을 위한 Input PNG 이미지들의 경로

## 제출양식: sample_submission.zip
- 추론한 PNG 이미지들은 zip 형식으로 압축된 제출 양식
- zip 파일 내부에 폴더 없이 이미지로만 구성
- 추론 결과 PNG 파일명 = 평가 입력 이미지 파일명 (PAIR)
