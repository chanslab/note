#LaTex

Obsidian은 **MathJax(LaTeX)** 를 기본적으로 지원하므로, `$공식$`(한 줄 수식) 또는 `$$공식$$`(중앙 블록 수식) 기호를 사용하여 깔끔하게 작성할 수 있습니다.

---

### 1. LaTeX 작성 기본 가이드 (Obsidian용)

- **인라인 수식:** 문장 중간에 `$x+y$`와 같이 작성합니다.
- **블록 수식:** 별도의 줄에 `$$...$$`로 감싸서 작성하며, 수식이 중앙에 크게 표시됩니다.
- **첨자:** 윗첨자(제곱)는 `^`, 아래첨자는 `_`를 사용합니다. (예: `$x^2$`, `$x_i$`)
- **그룹화:** 첨자가 여러 글자일 경우 `{}`로 묶습니다. (예: `$e^{x+y}$`)
    

---

### 2. 세부 분야별 기호 및 문법

#### ① 기초 산술 및 함수 (Basic Math)

AI의 손실 함수(Loss Function)나 데이터 변환에서 가장 기본이 되는 기호들입니다.

| **기호**     | **LaTeX 문법**    | **읽는 법**      | **AI에서의 의미 및 사용 예**             |
| ---------- | --------------- | ------------- | ------------------------------- |
| $\pm$      | `\pm`           | 플러스 마이너스      | 오차 범위, 신뢰 구간 표기                 |
| $\times$   | `\times`        | 곱하기           | 행렬의 차원($n \times m$) 표시         |
| $\div$     | `\div`          | 나누기           | 일반적인 나눗셈                        |
| $\sqrt{x}$ | `\sqrt{x}`      | 루트 $x$        | 표준 편차 계산, L2 거리 계산              |
| $\sum$     | `\sum`          | 시그마(Sigma)    | **합계**: MSE(평균제곱오차) 등 모든 데이터 합산 |
| $\prod$    | `\prod`         | 프로덕트(Product) | **곱하기**: 확률의 결합 확률 계산           |
| $\log$     | `\log`          | 로그(Log)       | 정보 엔트로피, 로지스틱 회귀의 손실 함수         |
| $\exp$     | `\exp` or `e^x` | 익스포넨셜         | 소프트맥스(Softmax) 함수, 가우스 분포       |

#### ② 선형대수학 (Linear Algebra)

데이터를 벡터와 행렬로 표현하는 AI의 뼈대입니다.

|**기호**|**LaTeX 문법**|**읽는 법**|**AI에서의 의미 및 사용 예**|
|---|---|---|---|
|$\mathbf{v}$|`\mathbf{v}`|벡터 v|데이터 포인트 하나 (특징 벡터)|
|$\mathbf{A}$|`\mathbf{A}`|행렬 A|전체 데이터셋 또는 레이어의 가중치(Weight)|
|$\cdot$|`\cdot`|도트(Dot)|**내적**: 두 벡터 간의 유사도(Cosine Similarity) 계산|
|$\mathbf{A}^T$|`\mathbf{A}^T`|A 트랜스포즈|**전치**: 행렬의 행과 열을 바꿈 (연산 차원 맞춤)|
|$\\|\mathbf{x}$|`\|\mathbf{x}\|`|노름(Norm)|벡터의 크기/길이. L1, L2 규제(Regularization)에 사용|
|$\approx$|`\approx`|근사하다|모델의 예측값이 실제값에 가까워짐을 표현|

#### ③ 미분 및 최적화 (Calculus & Optimization)

AI가 '학습'을 통해 가중치를 업데이트하는 원리입니다.

|**기호**|**LaTeX 문법**|**읽는 법**|**AI에서의 의미 및 사용 예**|
|---|---|---|---|
|$\frac{dy}{dx}$|`\frac{dy}{dx}`|d y, d x|일반 미분: 변화율 측정|
|$\partial$|`\partial`|라운드 디(Partial)|**편미분**: 특정 가중치($w$)가 오차에 주는 영향 계산|
|$\nabla$|`\nabla`|나블라/그레이디언트|**경사**: 오차가 가장 빨리 줄어드는 방향(경사하강법)|
|$\Delta$|`\Delta`|델타(Delta)|가중치의 변화량 또는 오차값|
|$\infty$|`\infty`|무한대|학습 반복 횟수나 극한값 표현|

#### ④ 확률 및 통계 (Probability & Statistics)

불확실성을 다루고 데이터의 분포를 이해하는 도구입니다.

![](https://encrypted-tbn3.gstatic.com/licensed-image?q=tbn:ANd9GcT0sJMt2MUeTpds1zLKRk93b5NwUG5pVWfldYu-4NztJ2KvNkC0KzBdX_TUvZixkexpfEu9lrJvPayJcK7sjDQ79lAAeBkaNgcTI6HFHAdrfba1lhI)

|**기호**|**LaTeX 문법**|**읽는 법**|**AI에서의 의미 및 사용 예**|
|---|---|---|---|
|$P(A)$|`P(A)`|P of A|사건 A가 발생할 확률|
|$P(A \mid B)$|`P(A \mid B)`|P of A given B|**조건부 확률**: B가 일어났을 때 A의 확률 (베이즈 정리)|
|$E[X]$|`E[X]`|기댓값 X|확률 변수의 평균적인 기대치|
|$\mu$|`\mu`|뮤(Mu)|데이터의 평균(Mean)|
|$\sigma$|`\sigma`|시그마(Sigma)|데이터의 표준편차(Standard Deviation)|
|$\sim$|`\sim`|따른다|특정 분포(예: 정규분포)를 따른다는 표시|

---

### 3. [최종 정리] Obsidian용 AI 수학 기호 마스터 표

| **구분**   | **기호**                          | **LaTeX 문법**                    | **읽는 법** | **주요 용도**                   |
| -------- | ------------------------------- | ------------------------------- | -------- | --------------------------- |
| **기초**   | $\sum_{i=1}^{n}$                | `\sum_{i=1}^{n}`                | 시그마      | 데이터의 총합 (Summation)         |
|          | $\prod$                         | `\prod`                         | 프로덕트     | 확률의 연속 곱 (Product)          |
|          | $                               | x                               | $        | `                           |
| **선형대수** | $\mathbf{W}$                    | `\mathbf{W}`                    | 행렬 W     | 가중치 행렬 (Weights)            |
|          | $\mathbf{x} \cdot \mathbf{y}$   | `\mathbf{x} \cdot \mathbf{y}`   | 내적       | 벡터 간 유사도 및 투영               |
|          | $\mathbf{A}^{-1}$               | `\mathbf{A}^{-1}`               | 역행렬      | 선형 방정식의 해 구하기               |
| **미분**   | $\frac{\partial L}{\partial w}$ | `\frac{\partial L}{\partial w}` | 편미분      | 가중치에 따른 손실값의 변화율            |
|          | $\nabla f$                      | `\nabla f`                      | 그레이디언트   | 다변수 함수의 기울기 벡터              |
| **확률**   | $\theta$                        | `\theta`                        | 세타       | 모델의 파라미터(매개변수) 총칭           |
|          | $\mathcal{N}$                   | `\mathcal{N}`                   | 가우시안/노멀  | 정규 분포 (Normal Distribution) |
|          | $\propto$                       | `\propto`                       | 비례한다     | 확률 밀도 함수 간의 관계 표현           |
