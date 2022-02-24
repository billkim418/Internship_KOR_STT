# Internship_KOR_STT
20210901 ~ 20211130 (주)소베텍 인턴십
# 소베텍 Internship(09-01 ~ 11/30) - 디지털 사업 본부
- 역활 : KOR-STT 한국어 음성인식 모델 연구
- 직책 : 인턴
- 진행기간 : 09_01 ~ 11/30
- 목표 : 한국어 음성인식 모델 개발
## 1. 한국어 음성인식 오픈 소스 라이브러리 검색
- 베이즈 딥러닝을 사용한 한국어 음성인식 모델
- Open-souce toolkit for end-to-end Korean library speech recognition -KoSpeech(2021)
- 칼디(kalid)를 이용하여 구축하는 한국어 오프소스 프로젝트 : Zeroth – NOW<br>
라는 3가지 오픈 소스 라이브러리를 선정하였다. 모든 모델은 장단점이 있었지만 범용성이 뛰어난 KoSpeech를 메인 모델로 선정하였다.
## 2. KoSpeech
한국어 오픈 소스 라이브러리 인 KoSpeech를 이용하여 음성인식 모델의 성능을 측정하고 이를 개선하는 것을 목표로 함.
KoSpeech안에는 여러 음성인식 모델들을 사용할 수 있는데 그 중 DeepSpeech2를 메인으로 삼아 성능을 측정
## 3. 진행 방법 : DeepSpeech2 논문 리뷰
- Activation function : ReLU
- Loss function : CTC LOSS
- Input : Vocabulary를 이용한 데이터 맵핑 구조를 가지고 있음(학습 전에 미리 생성)
- output : csv를 이용한 학습 결과 확인 및 Inference 가능
## 4. 시각화(Visualization)
- 결과 : main.log값에 나타나는 loss, log값으로는 학습의 진행상황을 확인할 수 없음. 따라서 PyTorch에 특화된 TensorboardX를 이용하여 loss, cer을 측정해 보았다.
- 처음부터 누적된 결과를 보고 싶었으나 초기 설정을 실패하여 일정 에폭 이후의 값을 아래 그림으로 첨부.
결과를 보면 loss 및 cer 값의 개선이 나타나지 않음을 확인 할 수 있다.
## 5. 피드백
- 개선해야할 점 : 3개월이라는 시간이 충분할줄 알았는데 리눅스, 파이토치 라는 새로운 기술 스택으로 인해 모델 적용 및 학습이 점점 늦춰졌다. 심지어 학습은 1달이 지나서야 가능했다.
- 또한 논문의 수리적 적용 구조를 파악하는데도 많은 시간이 소비 되었다. 하지만 이를 이용한다면 추후 파이토치를 용한 논문의 구현 및 모델 구조 수정이 용이 할 것이라 생각이 든다.



