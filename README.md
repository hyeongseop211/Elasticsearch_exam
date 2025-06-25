# ✅ TODO List 웹 애플리케이션

Flask, MySQL, Docker를 활용한 할 일 관리 웹페이지입니다.  
할 일을 **추가, 수정, 삭제, 완료**할 수 있으며,  
**카테고리 및 우선순위별**로 정리해 효율적인 일정 관리를 도와줍니다.

---

## 🔧 기술 스택

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

---

## 🚀 실행 방법

```bash
# 1. Docker 컨테이너 빌드 및 실행
docker-compose up --build
```

- 브라우저 접속: [http://localhost:5000](http://localhost:5000)

- `.env` 파일 생성 (루트 디렉토리에):

```
MYSQL_HOST=db
MYSQL_USER=root
MYSQL_PASSWORD=password
MYSQL_DB=todo_db
```

---

## 📁 프로젝트 구조

```
todo-app/
├── app.py                # Flask 메인 서버 파일
├── config.py             # DB 설정 정보
├── requirements.txt      # 설치할 Python 패키지
├── Dockerfile            # Flask 앱을 위한 Docker 설정
├── docker-compose.yml    # 전체 시스템 실행 정의
├── .env                  # 비밀번호 등 환경변수 저장
├── templates/
│   └── index.html        # HTML 화면
├── static/
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── main.js
└── routes/
    └── todo_routes.py    # Flask 라우터
```

---

## 📌 API 명세

### ✅ GET `/todos`  
- 전체 할 일 목록 반환  
- **Response 예시:**
```json
[
  {
    "id": 1,
    "title": "컴퓨터과학개론 과제 제출",
    "description": "6월 25일까지",
    "due_date": "2025-06-25T18:00:00",
    "priority": 3,
    "category": "학습",
    "is_completed": false
  }
]
```

### 🔍 GET `/todos/<int:id>`  
- 특정 할 일 조회

### ➕ POST `/todos`  
- 할 일 추가  
- **Request Body 예시:**
```json
{
  "title": "운동하기",
  "description": "헬스장 1시간",
  "due_date": "2025-06-26T20:00",
  "priority": 2,
  "category": "개인"
}
```

### 🛠 PUT `/todos/<int:id>`  
- 할 일 수정

### ❌ DELETE `/todos/<int:id>`  
- 할 일 삭제

### ✅ PATCH `/todos/<int:id>/complete`  
- 할 일 완료 여부 토글

---

## 👩‍💻 개발자 정보

- **이름**: 도유정  
- **소속**: 부경대학교 산업경영공학전공  
- **이메일**: [molmol1150@naver.com](mailto:molmol1150@naver.com)

---
