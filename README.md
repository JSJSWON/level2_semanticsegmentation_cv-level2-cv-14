# BoostCamp AI Tech4 level-2-재활용 품목 분류를 위한 Semantic Segmentation

## Member🔥
| [김지훈](https://github.com/kzh3010) | [원준식](https://github.com/JSJSWON) | [송영섭](https://github.com/gih0109) | [허건혁](https://github.com/GeonHyeock) | [홍주영](https://github.com/archemist-hong) |
| :-: | :-: | :-: | :-: | :-: |
| <img src="https://avatars.githubusercontent.com/kzh3010" width="100"> | <img src="https://avatars.githubusercontent.com/JSJSWON" width="100"> | <img src="https://avatars.githubusercontent.com/gih0109" width="100"> | <img src="https://avatars.githubusercontent.com/GeonHyeock" width="100"> | <img src="https://avatars.githubusercontent.com/archemist-hong" width="100"> |

## Index
* [Project](#project)
* [Team role](#team-role)
* [Procedures](#procedures)
* [Command](#command)
* [Wrap UP Report](#wrap-up-report)  

## Project
### 개요
- 배경: 쓰레기 대란, 매립지 부족과 같은 쓰레기로 인한 사회적 문제 해결 필요
- 주제: 재활용 품목 분류를 위한 Semantic Segmentation 모델 개발

<img width="150%" src="./image/model_visual.png"/>

- 기대 효과
    - 쓰레기장 설치 및 활용으로 분리수거의 정확도 향상
    - 아이들의 분리수거 교육에 활용
- Input: 쓰레기 객체가 담긴 이미지
- Output: segmentation 결과(pixel별 classification 결과)
- 카테고리: Backgroud, General trash, Paper, Paper pack, Metal, Glass, Plastic, Styrofoam, Plastic bag, Battery, Clothing

## Team role
- 김지훈: Augmentation 실험, Ensemble 구현 및 실험
- 원준식: baseline 작성, cross validation 실험
- 송영섭: mmseg를 위한 여러 Augmentation 구현 및 실험
- 허건혁: EDA를 위한 시각화 tool 개발,Copy Paste augmentation 실험
- 홍주영: multi-scale TTA , Pseudo-labeling 실험


## Procedures
대회 기간 : 2022.12.19 ~ 2023.01.05

| 날짜 | 내용 |
| :---: | :---: |
| 12.19 ~ 12.25 | BoostCamp 강의 수강 및 Segmentation 이론 학습|
| 12.26 ~ 01.01 | Data EDA & Model Experiment |
| 01.02 ~ 01.05 | HyperParameter Tuning & model Ensemble |


## Command
- train
```
python tools/train.py {config file}
```

- submission

```
python tools/inference.py {model} {checkpoint} --out {저장경로}
```

- streamlit
```
streamlit run visual/visual.py --server.port=[port 번호]
```

## Wrap UP Report
- [Report](https://wind-motorcycle-695.notion.site/Semantic-Segmentation-Wrap-Up-Report-CV-14-97f97b3b32b941c9828ff8a0abc64c6d)
