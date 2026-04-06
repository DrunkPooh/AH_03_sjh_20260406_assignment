# AH_03_sjh_20260406_assignment

# Pomodoro Timer & FastAPI Study

프론트엔드의 기초인 **자바스크립트 타이머** 구현과, 백엔드 프레임워크인 **FastAPI**의 기초 학습

---

## 1. Pomodoro Timer (Frontend)
사용자가 입력한 분 단위 시간을 바탕으로 카운트다운을 수행하는 웹 기반 타이머입니다.

### 주요 기능
- **시간 설정**: 사용자로부터 분(Minute) 단위를 입력받아 타이머 작동.
- **실시간 디스플레이**: `setInterval`을 이용해 1초마다 화면 갱신 (00:00 형식).
- **예외 처리**: 숫자 이외의 값 입력 방지 및 중복 실행 방지 알림.

### 파일 구성
- `index.html`: Bootstrap 5를 활용한 타이머 UI.
- `pomodoro.js`: 타이머 로직 및 DOM 조작.

---

## 2. User Management API (Backend)
Python의 **FastAPI**를 사용하여 구축한 간단한 REST API 서버입니다.

### 주요 엔드포인트 (API 명세)
| Method | Path | Description |
| :--- | :--- | :--- |
| **GET** | `/` | 서버 연결 확인 (Ping-Pong) |
| **GET** | `/hello` | 환영 메시지 출력 |
| **GET** | `/users` | 전체 사용자 목록 조회 |
| **GET** | `/users/{user_id}` | 특정 ID를 가진 사용자 상세 정보 조회 |
| **GET** | `/users/search` | 사용자 검색 기능 (개발 중) |

### 학습 포인트
- **Decorator (@)**: 파이썬 함수에 API 경로 기능을 부여하는 문법 학습.
- **Path Parameter**: URL 경로를 통해 변수(`user_id`)를 전달받는 방식 이해.
- **JSON Serialization**: 파이썬의 `List`, `Dict` 데이터를 JSON 형식으로 자동 변환하여 응답.

---

## 실행 방법 (How to Run)

### 프론트엔드 (Frontend)
1. `index.html` 파일을 브라우저로 엽니다.

### 백엔드 (Backend)
1. **가상환경 생성 및 활성화**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
