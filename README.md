# NLP Assignments

## 프로젝트 소개

이 저장소는 자연언어처리 과목에서 수행한 과제 노트북과 기말 프로젝트를 정리한 저장소입니다.

일반 과제에서는 텍스트 전처리, 토큰화, 한국어 형태소 분석, Word2Vec, 머신러닝 기반 분류, 딥러닝 기반 자연어처리 모델 등을 실습하였습니다.

기말 프로젝트에서는 텍스트 데이터를 기반으로 가짜/진짜 뉴스 또는 문장 분류를 수행하는 자연어처리 파이프라인을 구축하였습니다. 데이터의 노이즈를 분석하고, 전처리 규칙, 머신러닝 모델, BERT 계열 딥러닝 모델, 앙상블, 후처리 전략을 단계적으로 적용하여 성능을 개선하는 과정을 정리하였습니다.

## 주요 학습 내용

- 자연어 데이터 전처리
- 정규표현식을 활용한 텍스트 정제
- 한국어 형태소 분석 및 토큰화
- 단어 빈도 분석
- Word2Vec 기반 단어 임베딩
- TF-IDF 기반 텍스트 벡터화
- 머신러닝 기반 텍스트 분류
- BERT 기반 텍스트 분류
- RoBERTa, DeBERTa 계열 모델 활용
- K-Fold 교차 검증
- 하이브리드 앙상블
- 임계값 튜닝 및 후처리

## 프로젝트 구조

```text
nlp-assignments/
├── README.md
├── .gitignore
├── requirements.txt
├── notebooks/
│   ├── assignments/
│   │   ├── korean_sentiment_preprocessing.ipynb
│   │   ├── text_preprocessing_tokenization.ipynb
│   │   ├── bigram_language_model.ipynb
│   │   ├── ml_basics_regression_classification.ipynb
│   │   ├── word2vec_similarity.ipynb
│   │   ├── mlp_mnist_experiments.ipynb
│   │   ├── bilstm_attention_imdb.ipynb
│   │   ├── financial_phrasebank_mlp.ipynb
│   │   └── rnn_lstm_gru_bilstm_imdb.ipynb
│   └── final_project/
│       ├── 01_final_project_eda_baseline.ipynb
│       ├── 02_bert_noise_analysis.ipynb
│       ├── 03_duplicate_regex_rule.ipynb
│       ├── 04_hybrid_ensemble.ipynb
│       └── 05_threshold_postprocessing.ipynb
└── docs/
```

## 과제 노트북

| 파일명 | 내용 |
|---|---|
| `korean_sentiment_preprocessing.ipynb` | 한국어 텍스트 전처리, 정규표현식, 형태소 분석, 명사 추출 실습 |
| `text_preprocessing_tokenization.ipynb` | 자연어 전처리, 토큰화, NLTK 및 KoNLPy 활용 실습 |
| `bigram_language_model.ipynb` | Bigram 기반 언어 모델링 실습 |
| `ml_basics_regression_classification.ipynb` | 머신러닝 기반 회귀, 분류, 로지스틱 회귀 실습 |
| `word2vec_similarity.ipynb` | Word2Vec 모델 학습 및 단어 유사도 분석 |
| `mlp_mnist_experiments.ipynb` | MLP 기반 딥러닝 모델 실습 |
| `bilstm_attention_imdb.ipynb` | IMDB 데이터셋 기반 BiLSTM 및 Attention 모델 실습 |
| `financial_phrasebank_mlp.ipynb` | Financial PhraseBank 데이터셋 기반 금융 문장 분류 |
| `rnn_lstm_gru_bilstm_imdb.ipynb` | IMDB 데이터셋 기반 RNN, LSTM, GRU, BiLSTM 모델 비교 |

## 기말 프로젝트 개요

기말 프로젝트는 텍스트 분류 문제를 해결하기 위한 자연어처리 머신러닝/딥러닝 파이프라인을 구축하는 것을 목표로 하였습니다.

프로젝트의 핵심은 단순히 하나의 모델을 학습하는 것이 아니라, 데이터 내부에 존재하는 노이즈를 분석하고, 노이즈 유형에 따라 서로 다른 전략을 적용하여 최종 분류 성능을 개선하는 것입니다.

주요 흐름은 다음과 같습니다.

1. 데이터 구조 분석 및 노이즈 탐지
2. TF-IDF 기반 베이스라인 모델 학습
3. BERT 기반 딥러닝 모델 도입
4. 노이즈 데이터 패턴 분석
5. 중복 데이터 제거 및 정규표현식 기반 규칙 정의
6. RoBERTa, DeBERTa 기반 고성능 모델 학습
7. K-Fold 교차 검증 기반 앙상블
8. 임계값 튜닝 및 후처리

## 기말 프로젝트 노트북

| 파일명 | 내용 |
|---|---|
| `01_final_project_eda_baseline.ipynb` | 데이터 로드, EDA, 마침표 밀도 기반 노이즈 탐지, TF-IDF + Logistic Regression 베이스라인 모델 학습 |
| `02_bert_noise_analysis.ipynb` | BERT 모델 파인튜닝, 정상/노이즈 데이터 분리 예측, 노이즈 데이터의 단어 빈도, 글자 수, 불용어 비율 분석 |
| `03_duplicate_regex_rule.ipynb` | 중복 텍스트 제거, 노이즈 데이터의 문자열 패턴 분석, 정규표현식 기반 하드코딩 규칙 정의 |
| `04_hybrid_ensemble.ipynb` | RoBERTa, DeBERTa 계열 모델 활용, K-Fold 교차 검증, Clean/Noise 구간 분리 기반 하이브리드 앙상블 |
| `05_threshold_postprocessing.ipynb` | 예측 확률 기반 임계값 튜닝, 라벨 후처리, 순위 기반 flipping 전략 실험 |

## 기말 프로젝트 상세 설명

### 1. EDA 및 베이스라인 모델

첫 번째 단계에서는 데이터를 로드한 뒤 텍스트 구조를 분석하였습니다.

텍스트 내 단어 수 대비 마침표 개수를 계산하는 `period density` 지표를 사용하여 비정상적인 문장 구조를 가진 데이터를 노이즈 데이터로 분류하였습니다. 이후 노이즈를 제거한 Clean Data를 대상으로 TF-IDF 벡터화를 수행하고, Logistic Regression 모델을 학습하여 베이스라인 성능을 확인하였습니다.

### 2. BERT 기반 모델 및 노이즈 분석

두 번째 단계에서는 PyTorch와 Hugging Face Transformers를 활용하여 `bert-base-uncased` 모델을 파인튜닝하였습니다.

테스트 데이터 역시 마침표 밀도 기준으로 Clean 구간과 Noise 구간으로 나누었고, Clean 구간은 BERT 모델로 예측하였습니다. Noise 구간에 대해서는 단어 빈도, 문장 길이, 불용어 비율 등을 분석하여 라벨을 구분할 수 있는 추가적인 패턴이 존재하는지 확인하였습니다.

### 3. 중복 제거 및 정규표현식 규칙

세 번째 단계에서는 동일한 텍스트를 가진 중복 데이터를 제거하여 학습 데이터의 신뢰도를 높였습니다.

또한 노이즈 데이터 중 특정 문장부호로 끝나는 경우나, 의미 없는 외톨이 소문자가 포함된 경우 특정 라벨로 분류될 가능성이 높다는 점을 확인하고, 이를 정규표현식 기반 규칙으로 구현하였습니다.

### 4. 고성능 모델 및 하이브리드 앙상블

네 번째 단계에서는 `roberta-large`, `microsoft/deberta-v3-large` 등 더 강력한 사전학습 언어모델을 활용하였습니다.

Clean 데이터는 RoBERTa 계열 모델이 담당하고, 명확한 노이즈 패턴은 정규표현식 규칙으로 처리하였습니다. 규칙으로 판별하기 어려운 노이즈 데이터는 K-Fold로 학습한 DeBERTa 모델들의 예측 확률을 평균내는 Soft Voting 방식으로 처리하였습니다.

### 5. 임계값 튜닝 및 후처리

마지막 단계에서는 모델의 예측 확률을 기반으로 최종 라벨을 결정하는 임계값을 조정하였습니다.

기본 임계값 0.5만 사용하는 것이 아니라, 여러 임계값을 실험하여 F1 Score가 더 높아지는 구간을 탐색하였습니다. 또한 예측 확률의 순위를 기준으로 일부 라벨을 강제 변환하는 후처리 전략을 실험하였습니다.

## 실행 환경

본 저장소의 노트북은 Python 기반 Jupyter Notebook 환경에서 실행할 수 있습니다.

주요 사용 라이브러리는 다음과 같습니다.

- Python
- Jupyter Notebook
- NumPy
- pandas
- matplotlib
- seaborn
- scikit-learn
- NLTK
- KoNLPy
- gensim
- TensorFlow / Keras
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets


## 작성자

자연언어처리 과목 과제 및 기말 프로젝트 정리
