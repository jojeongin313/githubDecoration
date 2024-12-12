
# 데이터 분석 및 시각화 강의 요약 및 학습 계획

## Lecture 요약

### Lecture 13: 서울의 크리스마스 기온 분석
#### 핵심 내용
- 날짜 데이터를 `split()`으로 분리해 연도별 기온 분석.
- 연도별 평균 기온과 크리스마스 날씨 변화 시각화.
- 추세선을 통해 기온 변화의 패턴 분석.
    
#### 코드 예제
```python
import matplotlib.pyplot as plt

# 데이터
dates = ['2020-12-25', '2021-12-25']
temps = [1, -3]

# 날짜 데이터 처리
years = [int(date.split('-')[0]) for date in dates]

# 그래프
plt.plot(years, temps, marker='o', label='크리스마스 기온 변화')
plt.title('서울의 크리스마스 기온 변화')
plt.xlabel('연도')
plt.ylabel('기온(℃)')
plt.legend()
plt.grid()
plt.show()
```

---

### Lecture 14: 서울의 최저/최고 기온 분석
#### 핵심 내용
- 막대그래프와 박스그래프로 기온 데이터 분석.
- 박스그래프의 사분위수(Q1, Q3)와 이상치(outlier)의 의미 설명.

#### 코드 예제
```python
import matplotlib.pyplot as plt

# 데이터
max_temps = [10, 12, 14, 15, 13, 12, 10]

# 박스그래프
plt.boxplot(max_temps)
plt.title('최고 기온 데이터의 박스 그래프')
plt.show()
```

---

### Lecture 15: matplotlib bar()와 pie() 그리기
#### 핵심 내용
- `bar()`와 `pie()`로 막대 및 원그래프 생성.
- `autopct`와 `explode` 속성을 활용한 원그래프 비율 시각화.
- 누적 막대그래프로 여러 데이터 표현.

#### 코드 예제
```python
import matplotlib.pyplot as plt

# 원그래프
sizes = [40, 30, 20, 10]
labels = ['A', 'B', 'C', 'D']
explode = (0, 0.1, 0, 0)

plt.pie(sizes, labels=labels, explode=explode, autopct='%.1f%%', shadow=True)
plt.title('원그래프 예제')
plt.show()
```

---

### Lecture 16: 인구 데이터 준비와 지역의 연령별 인구 데이터 분석
#### 핵심 내용
- 행정안전부 데이터를 사용하여 특정 지역의 연령별 인구 분석.
- CSV 데이터를 읽어와 데이터 필터링 및 시각화.

#### 코드 예제
```python
import pandas as pd
import matplotlib.pyplot as plt

# 데이터 읽기
data = pd.read_csv('age.csv')
region = data[data['지역명'] == '서울']

# 그래프
plt.bar(region['연령'], region['인구수'])
plt.title('서울 연령별 인구수')
plt.xlabel('연령')
plt.ylabel('인구수')
plt.show()
```

---

### Lecture 17: 인구구조 연령별 성별 데이터분석
#### 핵심 내용
- 남성 데이터를 음수로 변환한 항아리 모양 그래프 생성.
- 문자열 처리와 데이터 필터링에 `replace()`와 조건문 사용.

#### 코드 예제
```python
male = [-30, -40, -50]
female = [30, 40, 50]

plt.barh(range(len(male)), male, label='남성', color='blue')
plt.barh(range(len(female)), female, label='여성', color='pink')
plt.title('항아리 그래프 예제')
plt.legend()
plt.show()
```

---

### Lecture 18: matplotlib의 scatter 그래프
#### 핵심 내용
- 산점도(`scatter()`)와 `colorbar()`로 데이터의 관계와 범주 시각화.
- 데이터 투명도(`alpha`)와 크기(`s`) 설정.

#### 코드 예제
```python
x = [1, 2, 3, 4]
y = [4, 5, 6, 7]
sizes = [100, 200, 300, 400]

plt.scatter(x, y, s=sizes, alpha=0.5, c=sizes, cmap='viridis')
plt.colorbar()
plt.title('산점도 시각화')
plt.show()
```

---

### Lecture 19: VS Code에서 노트북 활용
#### 핵심 내용
- VS Code에서 Python 노트북 실행 및 디버깅 방법.
- matplotlib와 numpy 활용 예제 작성.

#### 코드 예제
```python
import matplotlib.pyplot as plt

x = range(10)
y = [i ** 2 for i in x]

plt.plot(x, y)
plt.title('VS Code 실행 예제')
plt.show()
```

---

### Lecture 20-22: 서울 지하철 데이터 분석
#### 핵심 내용
- `replace()`와 `astype()`으로 쉼표 제거 후 데이터 정제.
- 시간대별 승하차 데이터를 분석해 막대그래프 및 원그래프로 시각화.

#### 코드 예제
```python
# 시간대별 승차 데이터
hours = ['7시', '8시', '9시']
passengers = [300, 500, 400]

plt.bar(hours, passengers, color='orange')
plt.title('시간대별 승차 인원')
plt.show()
```

---

### Lecture 23: 과학 컴퓨팅 패키지 Numpy
#### 핵심 내용
- `arange`, `linspace`로 배열 생성.
- `reshape`, `expand_dims`로 배열의 모양 변환.

#### 코드 예제
```python
import numpy as np

arr = np.arange(1, 10).reshape(3, 3)
print("원본 배열:\n", arr)

arr_expanded = np.expand_dims(arr, axis=0)
print("차원 추가 배열:\n", arr_expanded)
```

---

## 학습 계획

### 1단계: 주요 개념 학습 (1.5시간)
#### 데이터 시각화 (40분)
- Lecture 13-15: matplotlib 꺾은선, 박스, 원그래프 연습.
- 코드를 직접 작성하고 결과 분석.

#### 데이터 분석 기법 (40분)
- Lecture 16-20: CSV 데이터 정제, 산점도와 항아리 그래프 연습.
- `replace()`, `map()` 등을 활용한 데이터 처리.

#### Numpy와 VS Code (30분)
- Lecture 19, 23: Numpy 배열 생성과 VS Code 환경 설정 학습.

---

### 2단계: 복습 및 요약 정리 (40분)
#### 핵심 코드 복습 (20분)
- 모든 강의의 핵심 코드를 다시 작성하며 이해.

#### 요약 노트 정리 (20분)
- 각 주제별 요약 내용을 검토하며 암기.
