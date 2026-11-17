## 안녕하세요, 류현준입니다 👋

**생성형 AI를 실제 현업 문제에 붙이고, 그 결과를 숫자로 검증하는 ML 엔지니어**를 목표로 하는 전자컴퓨터공학과 학부 연구생입니다.

웹툰 제작사 산학협력 과제와 정부 지원 연구과제를 수행하며, 모델을 학습하는 것보다 **"이 결과를 믿어도 되는가"**를 확인하는 데 더 많은 시간을 썼습니다.

---

### 🔬 Research & Projects

| 프로젝트 | 내용 | 핵심 결과 |
|---|---|---|
| [**Webtoon Style LoRA**](https://github.com/guswns578/webtoon-style-lora)<br><sub>산학협력 과제 · 1인 담당</sub> | 웹툰 작가 선화 스타일과 캐릭터 8명 SDXL LoRA 학습, 4축 정량 평가, 제작사 납품용 컷 생성 도구 | CCIP 캐릭터 판별 균형 정확도 95.4%, 포즈 지표 거짓 성공 발견·수정, Studio v1.3 배포 |
| [**Ink Transfer Net**](https://github.com/guswns578/ink-transfer-net)<br><sub>산학협력 후속 연구</sub> | 선 위치는 그대로 두고 잉크 표현만 바꾸는 결정론적 선화 변환 모델 | 구조 변경으로 선 소실 10.74% → 0.008%, 병목을 데이터 품질로 규명 |
| [**Fashion VTON Research**](https://github.com/guswns578/fashion-vton-research) | 1인 브랜드 쇼핑몰 상품 착용 이미지 생성: 평가 체계, 3D 의상 기하, 판매자 정체성 생성, 12GB 로컬 VTON | 정체성 유사도 22% → 94%, 보호 영역 변화 0픽셀 합성, 테스트 80개 |
| [**Upper-Body Action Recognition**](https://github.com/guswns578/upper-body-action-recognition)<br><sub>정부 과제 · 진행 중</sub> | 화상 대화 영상의 상반신 행동 실시간 인식 모듈 | 개발셋 누수(0.48 vs 0.15) 발견·수정, 인과 TCN mAP 0.186 (우연 수준 0.032) |

---

### 🛠 Tech Stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)

**ML / Frameworks**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![ONNX Runtime](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat-square&logo=onnx&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Gradio](https://img.shields.io/badge/Gradio-F97316?style=flat-square)
![ComfyUI](https://img.shields.io/badge/ComfyUI-1A1A1A?style=flat-square)

**Infra / Tools**

![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Blender](https://img.shields.io/badge/Blender-F5792A?style=flat-square&logo=blender&logoColor=white)
![NVIDIA](https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)

---

### 🧠 Models I've Worked With

| 분야 | 모델 · 기법 | 어떻게 다뤘나 |
|---|---|---|
| 이미지 생성 | SDXL, LoRA / LoCon / DoRA, ControlNet, IP-Adapter | Kohya로 직접 학습, 캡셔닝 설계, 추론 조건 통제 비교 |
| 가상 피팅 | IDM-VTON, FASHN VTON 1.5 | 12GB GPU용 ComfyUI 노드 구현, 보호 합성 파이프라인 |
| 분할 · 검출 | SAM, GroundingDINO, DensePose, YOLOX | 마스크 전처리, 디자인 보호 마스크 |
| 포즈 · 행동 | RTMPose / RTMW, OpenPose, MediaPipe, ST-GCN++, Video Swin | 추출기 비교로 선정, 공개 모델 원인 분리 진단 |
| 직접 설계 · 학습 | 인과 TCN / GRU, 픽셀 공간 잔차 네트워크 | MMA-52 행동 인식 학습, 결정론적 선화 변환 |
| 평가 | CCIP, CSD, SFace, DWPose 기반 포즈 지표 | 도메인에 맞게 임계값 재보정, 지표 자체의 거짓 성공 검증 |
| 3D | GarmentCode, Blender 천 시뮬레이션 | 치수 → 패턴 → 시뮬레이션 → 조건 맵 파이프라인 |

---

### 🧭 How I Work

- **한 번에 한 변수만** 바꾸고, 같은 seed·조건에서 비교합니다.
- **지표도 검증합니다.** 포즈 지표가 실패한 결과를 통과시키거나, 개발셋이 같은 사람으로 오염된 경우를 직접 찾아 고쳤습니다.
- **실행 성공과 품질 성공을 구분합니다.** 안 된 실험도 이유와 함께 기록하고, 근거가 약하면 결론을 내리지 않습니다.
- 구현 속도는 AI 코딩 도구로 높이고, 실험 설계와 결과 해석은 직접 합니다.

---

### 📫 Contact

- Email: guswns253401@skuniv.ac.kr
