# IMAGENET

## 주요 내용:
  <br>-torch: 딥러닝 핵심 엔진 (텐서, GPU, 자동미분)

  <br>-torch.nn: 신경망 구축 도구 (레이어, 손실함수, 모델)

  <br>-torchvision: 컴퓨터 비전 전용 (모델, 변환, 데이터셋)

  <br>-requests: HTTP 통신 (파일 다운로드, API 호출)

  <br>-json: 데이터 교환 (설정 파일, 어노테이션)


 ## 7. Ultralytics
https://docs.ultralytics.com/ko/models/yolov8/  --> yolo v8
<img width="1162" height="568" alt="화면 캡처 2025-07-16 111022" src="https://github.com/user-attachments/assets/17dac8ec-cd1e-4733-b36f-5f812f57001d" />
<img width="685" height="477" alt="화면 캡처 2025-07-16 104326" src="https://github.com/user-attachments/assets/96d6c35e-fc0f-4561-ba66-a54129f08729" />


# 📚 YOLOv8 용어 정리

YOLOv8 (You Only Look Once version 8)은 Ultralytics에서 개발한 실시간 객체 탐지(Object Detection), 세분화(Segmentation), 추적(Tracking) 모델입니다. 본 문서는 YOLOv8에서 자주 사용되는 핵심 용어들을 정리한 것입니다.

---

## 📌 기본 용어

| 용어 | 정의 | 설명 |
|------|------|------|
| **YOLO** | You Only Look Once | 하나의 패스로 객체를 탐지하는 실시간 딥러닝 탐지 모델 |
| **Ultralytics** | 개발사 | YOLOv8을 포함한 여러 YOLO 버전을 개발한 회사 |
| **Bounding Box** | 경계 상자 | 이미지에서 객체의 위치를 나타내는 네모 |
| **Confidence** | 신뢰도 | 모델이 객체라고 판단한 확률 값 (0~1) |
| **Class** | 클래스 | 객체 종류 (예: 사람, 자동차, 고양이 등) |
| **IoU** | Intersection over Union | 예측 박스와 실제 박스의 겹치는 정도 |
| **NMS** | Non-Maximum Suppression | 겹치는 박스를 제거하고 최적의 박스만 남김 |

---

## 🛠️ 파일 및 경로

| 용어 | 정의 | 설명 |
|------|------|------|
| **`data.yaml`** | 데이터 구성 파일 | 클래스 이름과 이미지 경로(train/val) 등을 설정 |
| **`runs/detect`** | 탐지 결과 저장 경로 | 예측 결과 이미지와 `.txt` 파일이 저장되는 기본 폴더 |
| **weights** | 가중치 파일 | 학습된 모델 파라미터 (예: `yolov8n.pt`) |

---

## 🎓 모델 구성

| 용어 | 정의 | 설명 |
|------|------|------|
| **yolov8n** | nano | 가장 가벼운 YOLOv8 모델 |
| **yolov8s** | small | 소형 모델 |
| **yolov8m** | medium | 중형 모델 |
| **yolov8l** | large | 대형 모델 |
| **yolov8x** | extra large | 가장 큰 모델 |

> 일반적으로 `n → s → m → l → x` 순으로 정확도는 올라가고 속도는 느려짐

---

## 🧠 학습 관련

| 용어 | 정의 | 설명 |
|------|------|------|
| **Epoch** | 학습 반복 횟수 | 전체 데이터셋을 몇 번 반복 학습할지 |
| **Batch Size** | 배치 크기 | 한 번에 학습에 사용하는 이미지 개수 |
| **LR (Learning Rate)** | 학습률 | 가중치를 업데이트할 때 변화량의 크기 |
| **Optimizer** | 최적화 알고리즘 | 가중치를 조절하는 방법 (예: SGD, Adam 등) |
| **Loss** | 손실 함수 | 모델이 얼마나 틀렸는지를 수치로 표현 |
| **Overfitting** | 과적합 | 학습 데이터에는 잘 맞지만 실제 데이터에는 성능이 떨어지는 현상 |

---

## 📤 출력/결과

| 용어 | 정의 | 설명 |
|------|------|------|
| **`labels`** | 탐지 결과 텍스트 파일 | `[class_id, x_center, y_center, width, height]` 형식 |
| **mAP (mean Average Precision)** | 평균 정밀도 | 모델의 정확도 척도 |
| **TP / FP / FN** | True/False Positive/Negative | 탐지 평가 지표 |
| **F1 Score** | 조화 평균 | Precision과 Recall의 조화 평균 |

---



