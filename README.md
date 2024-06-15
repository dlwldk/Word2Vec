# Word2Vec 임베딩
word2vec 모델을 사용한 단어 임베딩 구현

## 설명

목표는 유사성을 가진 target 단어와 context 단어로 구성된 30개의 단어 쌍을 생성
word2vec 모델을 사용하여 훈련 데이터의 모든 단어에 대한 임베딩 벡터를 찾고 모델은 다음 하이퍼파라미터를 사용하여 확률적 경사 하강법(SGD) optimizer 선택
- hidden layer dimension: 5
- learning rate: 0.1
- epochs: 150

## 프로세스

1. **데이터 생성**:
    - 지리적 데이터를 사용하여 국가와 해당 국가의 수도를 연결하는 훈련 데이터를 생성
    - 각 쌍은 target 단어로 특정 국가를, context 단어로 해당 국가의 수도로 지정

2. **모델 훈련**:
    - 지정된 hyperparameter을 사용하여 SGD 옵티마이저로 word2vec 모델을 구현
    - 더 나은 결과를 얻기 위해 hyperparameter을 조정

3. **시각화**:
    - 수렴을 보여주기 위해 epoch 수에 따른 loss를 플롯팅
    - t-SNE 시각화를 사용하여 2차원 공간에 모든 결과 벡터를 플롯팅
    - 유사한 단어는 embedding 공간에서 가깝게 위치

## 환경 및 라이브러리
- Python 3.6+
- NumPy
- Scikit-Learn
- Matplotlib
