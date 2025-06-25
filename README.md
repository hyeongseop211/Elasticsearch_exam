# TODO List 웹 페이지

Flask와 MySQL Workbench, Docker로 구현한 todo list 관리 웹페이지입니다.
할 일 목록을 추가, 수정, 삭제하고, 카테고리와 우선순위 별 관리가 가능합니다.


## How to Run

1. 아래 명령어로 Docker 컨테이너를 실행하세요.

docker-compose up --build

2. 브라우저에서 아래 주소로 접속하세요.

http://localhost:5000

3. .env 파일을 루트 디렉토리에 생성하고 아래 내용을 설정하세요.

MYSQL_HOST=db
MYSQL_USER=root
MYSQL_PASSWORD=password
MYSQL_DB=todo_db

4. 프로젝트 구조

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

5. API 문서

GET/todos
할 일 전체 목록 반환
Response: JSON 배열

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

GET /todos/int:id
특정 할 일 조회

POST /todos
할 일 추가
Body (JSON):

{
  "title": "운동하기",
  "description": "헬스장 1시간",
  "due_date": "2025-06-26T20:00",
  "priority": 2,
  "category": "개인"
}

PUT /todos/int:id
할 일 수정

DELETE /todos/int:id
할 일 삭제

PATCH /todos/int:id/complete
할 일 완료 여부 토글

기술 스택
Backend: Flask

Frontend: HTML5, CSS3, JavaScript

Database: MySQL Workbench

Infra: Docker, Docker Compose


### 개발자

이름: 도유정

소속: 부경대학교 산업경영공학전공

이메일: [molmol1150@naver.com]

