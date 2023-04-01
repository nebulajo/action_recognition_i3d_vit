# Three-Stream I3D: ViT 기반의 Attention Stream을 활용한 Action Recognition 연구 

Action Recognition 이란 Video의 전체 프레임에서 서로 다른 동작을 구별해 내는 task이다. Action Recognition 연구에서는 Two-Stream I3D 모델이 베이스라인으로 사용되며, 이는 Inception V1의 2D ConvNet 이 3D ConvNet으로 전환된 구조이다. 서로 다른 두 가지 특징인 RGB와 Optical Flow를 개별적인 네트워크를 통해 학습을 진행하며, 두 Stream의 Class Score의 평균값을 사용한다. 본 연구에서는 최근 각광받고 있는 Vision Transformer를 기존의 Two-Stream I3D 모델에 적용한 Three-Stream I3D를 제안한다. Two Stream에 Attention Stream을 추가하여 Attention Value를 반영한다. 제안하는 방법론의 검증을 위해 UCF-101과 HMDB-51 데이 터셋을 통해 기존의 Two-Stream I3D와 비교 실험을 진행하였으며, 제안하는 방법론의 우수성을 검증하였다.

## Architecture

<img width="649" alt="스크린샷 2023-04-01 오후 2 42 30" src="https://user-images.githubusercontent.com/126544082/229267913-51581066-578b-40a9-b680-8efeab151c44.png">

## Experiment

본 논문에서는 ViT 를 활용하여 특정 객체의 움직임에 주목하는 Action Recognition 연구를 수행하였다. Attention Value
를 계산하는 Attention Stream 구조를 Two-Stream 구조에 결합한 Three-Stream I3D 구조를 제안하였다. 연구 결과 UCF101, HMDB-52 데이터셋에서 기존의 모델보다 더 높은 성능을 보임을 확인하였다. 이를 통해 Three-Stream I3D 구조가 특정 객체의 움직임에 주목하여, Two-Stream I3D 구조보다 더 높은 성능을 이끌어 내는 것을 확인하였다.
