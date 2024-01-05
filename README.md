# sasang_Diagnosis

COVID-19 Interpretable Diagnosis Algorithm Based on a Small Number of Chest X-Ray Samples 논문 기반 데이터 증강기법 사용

ABSTRACT


<문제>

COVID-19에 기반한 개인 흉부 X-선(CXR)을 사용한 의료 진단 방법은 초기 연구에서 어려움을 겪었음
→ COVID-19 감염자의 CXR 데이터를 식별하는 데 어려움
→ 연구 초기에는 감염자의 CXR 데이터가 부족

<해결>

인공 지능(AI)과 의료 진단의 결합
→ AI 모델의 해석 가능성 분석을 사용하여 COVID-19에 감염된 CXR 샘플의 병변 특성을 탐색하고 의료 진단을 지원
오버피팅을 피하기 위해 데이터 증가 기법을 사용해 데이터셋 확장
전이학습
→ 다양한 사전 훈련된 모델을 테스트
→ 소수 샘플로 모델 훈련을 완료하기 위해 독특한 출력 레이어를 설계


<결과>

세 가지 다른 출력 레이어에서 네 가지 사전 훈련된 모델의 출력 결과를 비교
데이터 증가 후의 결과를 원래 데이터셋의 결과와 비교
24개 그룹의 독립적인 테스트를 수행하기 위해 제어 변수 방법 사용
→ 99.23%의 정확도와 98%의 리콜률이 얻어지고 CXR 해석 가능성 분석의 시각적 결과가 표시

<정리>

COVID-19 진단 알고리즘 네트워크는 높은 일반화 및 가벼운 특성을 가짐.
→ 빠른 속도로 다른 작업에 적용 가능
→ 실험 데이터가 부족한 경우에도 유용
해석 가능성 분석은 의료 진단에 새로운 가능성을 제공

## RELEVANT WORK
1.1 COVID-19와 VGGNet
의료와 AI의 결합의 가장 중요한 기여는 의사들의 반복된 작업을 줄이는 데 있으며, 적절한 네트워크는 흉부 엑스레이 데이터를 통해 정상과 감염된 개인을 높은 정확도로 구별 가능

깊은 합성곱 신경망으로, 합성곱 신경망의 깊이와 성능 간의 관계를 탐구

3×3 합성곱 커널과(합성곱 신경망에서 사용되는 필터의 크기) 2×2 최대 풀링 레이어를 반복적으로 쌓아 16~19개의 레이어로 이루어진 합성곱 신경망을 구축

3 × 3 합성곱 코어와 2 × 2 풀링 코어를 사용하여 네트워크 구조를 깊게 만들어 성능을 향상시킴

네트워크 레이어의 증가는 매개 변수의 폭발을 일으키지 않음 —> 매개변수는 주로 마지막 세 개의 완전 연결 레이어에 집중되기 때문


https://velog.io/@skysh0929/COVID-19-Interpretable-Diagnosis-Algorithm-Based-on-a-SmallNumber-of-Chest-X-Ray-Samples


## CNN
![cnn](https://github.com/degull/sasang_Diagnosis/assets/99521386/77cb3c95-afc3-47d6-bbee-5bd55349a5bd)
** 이미지 분류를 위한 Convolutional Neural Network(CNN) 
* 총 247개의 이미지가 5개의 클래스로 분류되기 위해 사용
* 전체 모델은 약 11백만 개의 파라미터를 가지며, 이는 약 42.61MB의 메모리를 차지
* 이미지를 입력으로 받아, 5개의 다른 클래스 중 하나로 분류하는 작업을 수행
