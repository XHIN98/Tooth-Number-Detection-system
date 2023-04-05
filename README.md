# 프로젝트 이름
튼튼하니, 튼튼한 이(object detection)

# 프로젝트 소개
치아구조와 치아식별을 위한 객체탐지 시스템 모델 개발

# 프로젝트 개요/동기
- 우리나라 연령대가 점점 높아지고 있으며, 실버산업이 확장되고 있는 추세가 보임.
- 시장분석을 해보니 인공지능으로 확장성이 높은 분야는 의료분야이다.
![image](https://user-images.githubusercontent.com/111558519/229974001-6e290b77-6ae1-44a1-b2f4-d095b084c33b.png)
- 외래 다빈도 상병 순위별 현황: 치은염 및 치주질환이 33% 차지
- 연령별 치주질환 진료인원 50 ~ 70대가 많음
![image](https://user-images.githubusercontent.com/111558519/229974009-e85c58db-fa16-4dcb-84a3-fbb6262b2e49.png)
- 특히 부산에 구강질환 환자가 증가하고 있으며, 구강관리에 도움되는 어플의 성능형상 시 긍정적인 효과가 발생
![image](https://user-images.githubusercontent.com/111558519/229974290-c598eb28-ad4c-4d27-8596-4df668f034b0.png)
### 효과 
- 치과 = 친숙
- 환자 수 증가 = 이익 증대
### 사업 확장 가능성
- 부산시 뿐만 아니라 전국적으로 확장 가능성이 증가




# 기술 스택
<p>
  <img src="https://img.shields.io/badge/python-3776AB?style=flat-square&logo=Python&logoColor=white"/>
   <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=PyTorch&logoColor=white"/>
   <img src="https://img.shields.io/badge/Google Colab-F9AB00?style=flat-square&logo=Google Colab&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=Jupyter&logoColor=white"/>
<img src="https://img.shields.io/badge/YOLO-00FFFF?style=flat-square&logo=YOLO&logoColor=white"/>
</p>

# 데이터 수집 및 가공
1. 데이터 수집 및 가공은 대회에서 제공. (DATASET: 1741)
![1123123](https://user-images.githubusercontent.com/111558519/229976208-d6de7fef-eb99-4031-a7fe-dd79f2b70be9.GIF)


# 데이터 모델링 및 학습 절차
### 데이터 모델링
 - 기본적으로 데이터 모델링을 할 때 YoLo의 yolov5 모델을 사용했습니다.
 - yolov5 레퍼지토리에서 코드 다운
 - img: 입력 이미지 크기
 - batch: 배치사이즈
 - epochs: 총 학습 에폭
 - data: 데이터겟 yaml 파일 경로
 - weights: 모델 웨이트 경로
 - cache: 캐시 이미지
![모델학습 yolov5](https://user-images.githubusercontent.com/111558519/229989741-a3b058ac-840e-4d02-a334-1bfeefa06aa4.GIF)
- 학습 파라미터들을 지정해주고 모델을 학습했다. epoch 만큼 학습을 진행하고 나면 학습이 종료되고 'Result saved to runs/train/exp'라는 문구가 뜨는데 이 경로에 학습한 정보가 저장이 되어 있다는 뜻임 exp 몇번에 저장되었는지 확인 필요.

### 학습한 모델을 테스트
![모델 테스트](https://user-images.githubusercontent.com/111558519/229992874-8fa6cd87-29d5-4614-ab44-2e2b82c7bdb1.GIF)
- 학습한 모델을 테스트함. 테스트가 끝나고 테스트 정보가 저장된 경로가 나오는데 이 exp번호를 확인해야 했었다.
- 테스트 결과를 확인 코드를 실행함.
![image](https://user-images.githubusercontent.com/111558519/229993693-dae95f3b-436e-4031-a3b6-c56d1783b96b.png)

## 학습한 모델을 테스트하고 정밀도와 재현율 검사
![image](https://user-images.githubusercontent.com/111558519/229993872-476316f2-0fbf-4916-8beb-3a789634b039.png)

# 결과
![image](https://user-images.githubusercontent.com/111558519/229993908-76147dc0-719b-4a4b-8c14-238cfa76212f.png)
![image](https://user-images.githubusercontent.com/111558519/229993926-1573c78d-ae1f-47ae-a2e6-3a3e367f28cc.png)

# 프로젝트를 활용한 서비스
- 딥러닝과 빅데이터를 활용한 치주질환 관리 플랫폼 기술 개발
- 치의학 의료 데이터 인공지능 의료기기 개발 가능
- 증상, 질병 이미지로 전문치료를 검색 및 환자에게 가장 적합한 치료법 제시 가능
- 다양한 이미지 인식 및 영상 인식 등을 이용한 새로운 형대의 서비스 출시

# 서비스 사용으로 인해 얻을 수 있는 긍정적인 효과
- 인건비 절약
- 높아진 영상데이터 질
- 정확도 상승
- 어플 사용률
- 질병 완화

# 기대효과
- 교정 치료 시 필요한 해부학적 랜드마크 자동 주석, 치아 자동 분할
- 치아우식, 치주염, 매복치, 가성낭종 등 자동으로 병소 검출
- 이전 치료내영 포함 자동 차팅
- 교정 시뮬레이션 및 성장 단계 모니터링
- 자동 보철물 디자인을 통한 이상적인 3D 수복물 자동 디자인 및 마진 표시, 환자 맞춤 스마일 라인 디자인
- 보험사기 의심 케이스 자동 체크를 통한 보험사기 예방

# 배운 점 & 아쉬운 점

### 이번에는 pytorch를 이용하여 객체 탐지 모델을 개발하였다.
1. 학습 파이프라인이 기존의 detection 모델들에 비해 간단하기 때문에 학습과 예측 속도가 빨랐다.
2. image calssification 보다 성능면에서 확실히 뛰어났다.
- 이유: 이미지 전체를 한번에 바라보는 방식을 이용하여 class에 대한 이해보다 높기 때문이다.

### mAP
AP는 precision과 recall을 그래프로 나타내었을 때의 면적이다.
- precision: 모델이 정답이라고 답한것들
- recall: 실제 정답들

### fps
- frame이 더 많을수록 움직임이 끊기지 않고 좀 더 자연스럽게 object detection이 가능하다.
- object detectrion에서의 fps라는건 초당 detectrion하는 비율을 의미하는것을 알게 되었다.
- frame을 dectection하는데 걸리는 시간을 inference time이라고 한다. 
- inference time이 오래걸리는 object detectrion 모델을 쓰게 된다면, 하나의 frame을 처리하고 있는데 어떤 물체가 갑자기 뛰어든다면 detection을 못할 확률이 커진다는 것을 알게 되었다.

- 다만 아쉬운점은 데이터의 양이 1741개라서 모델구성의 정밀도와 재현율이 조금 낮게 나온 것 같았다.
- 만약 데이터의 양과 정제가 더 잘되었다면, 현재 보이는 정밀도 재현율에서 긍정적인 효과를 보일 것으로 예상된다.

