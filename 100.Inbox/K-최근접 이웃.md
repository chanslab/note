어떤 데이터에 대한 답을 구할 때 주위의 다른 데이터를 보고 다수를 차지하는 것을 정답으로 사용

```python
from sklearn.neighbors import KNeighborsClassifier

kn = KNeighborsClassifier()

kn.fit(fish_data, fish_target)
kn.score(fish_data, fish_target)

kn.predict([[30, 600]]) # 리스트의 리스트로 전달
```

데이터가 아주 많은 경우 사용하기 어려움
> 데이터가 크기 때문에 메모리가 많이 필요하고 직선거리르 계산하는 데도 많은 시간이 필요



