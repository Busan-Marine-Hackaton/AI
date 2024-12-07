# AI 프로젝트

## 🚀 프로젝트 개요
크루즈 해커톤에서 개발된 **YOLOv8 기반 AI 모델**입니다. 이 프로젝트는 특정 객체 탐지 및 분석 작업을 수행하기 위해 설계되었습니다.

---

## 📂 파일 구조
```
├── AI/                   # AI 관련 코드와 데이터
├── labels/               # 데이터 라벨링 파일
├── train_results/        # 학습 결과 저장
├── .gitignore            # Git에서 무시할 파일 목록
├── README.md             # 프로젝트 설명 파일
├── data.yaml             # 데이터셋 설정 파일
├── hyp.yaml              # 학습 하이퍼파라미터 설정
├── yolov8n.pt            # YOLOv8 모델 가중치 파일
```

---

## 🔧 주요 기능
1. **YOLOv8 모델 활용**: 객체 탐지 및 분류 작업 수행
2. **데이터 라벨링 지원**: 라벨링 데이터는 `labels/` 디렉토리에 저장
3. **학습 결과 확인**: 학습 결과 파일은 `train_results/` 디렉토리에 저장

---

## 🛠️ 설치 및 실행 방법
1. **필수 라이브러리 설치**:
   ```bash
   pip install -r requirements.txt
   ```
2. **모델 학습 시작**:
   ```bash
   python train.py --data data.yaml --cfg yolov8n.yaml --weights yolov8n.pt --epochs 50
   ```
3. **모델 평가**:
   ```bash
   python detect.py --weights yolov8n.pt --source your_data/
   ```

---

## 📊 학습 결과
- 학습 중 생성된 로그와 결과는 `train_results/` 디렉토리에서 확인할 수 있습니다.
- YOLO 모델 성능 지표(Precision, Recall 등)는 `train_results/`에 저장됩니다.
