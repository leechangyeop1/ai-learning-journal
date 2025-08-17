# Logistic Regression

## 개념
로지스틱 회귀(Logistic Regression)는 이진 분류 문제를 해결하기 위해 사용되는 통계적 방법입니다. 입력 변수와 출력 변수 간의 관계를 모델링하여, 주어진 입력에 대해 특정 클래스에 속할 확률을 예측합니다. 로지스틱 회귀는 선형 회귀의 확장으로 볼 수 있으며, 출력값이 0과 1 사이의 확률로 제한됩니다.

## 수식
로지스틱 회귀의 기본 수식은 다음과 같습니다:

P(Y=1|X) = 1 / (1 + e^(-z))

여기서 z는 다음과 같이 정의됩니다:

z = β0 + β1X1 + β2X2 + ... + βnXn

- P(Y=1|X): 주어진 입력 X에 대해 Y가 1일 확률
- β0: 절편(intercept)
- β1, β2, ..., βn: 각 입력 변수에 대한 계수(coefficient)
- X1, X2, ..., Xn: 입력 변수

## 적용 방법
1. **데이터 준비**: 입력 변수(X)와 출력 변수(Y)를 준비합니다.
2. **모델 학습**: 주어진 데이터를 사용하여 로지스틱 회귀 모델을 학습합니다. 일반적으로 최대 우도 추정(Maximum Likelihood Estimation, MLE)을 사용하여 계수를 추정합니다.
3. **예측**: 학습된 모델을 사용하여 새로운 데이터에 대한 예측을 수행합니다. 예측된 확률을 기준으로 클래스 레이블을 결정합니다.
4. **모델 평가**: 정확도, 정밀도, 재현율 등의 지표를 사용하여 모델의 성능을 평가합니다.

## 예제
다음은 Python을 사용하여 로지스틱 회귀 모델을 구현하는 간단한 예제입니다:

```python
import numpy as np
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score

# 데이터 로드
data = pd.read_csv('data.csv')
X = data[['feature1', 'feature2']]
y = data['target']

# 데이터 분할
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# 모델 학습
model = LogisticRegression()
model.fit(X_train, y_train)

# 예측
y_pred = model.predict(X_test)

# 정확도 평가
accuracy = accuracy_score(y_test, y_pred)
print(f'Accuracy: {accuracy:.2f}')
```

로지스틱 회귀는 간단하면서도 강력한 분류 알고리즘으로, 다양한 분야에서 널리 사용됩니다.