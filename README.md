# 🥔 감자마켓 (GAMZA Market)

따뜻한 동네 이웃 간의 중고거래 & 나눔 플랫폼 **감자마켓**입니다.

---

## 🌟 주요 기능

- **중고 물품 목록 및 필터링**
  - 실시간 상품 목록 조회 및 카테고리별 탐색
  - 판매 상태(판매중, 예약중, 거래완료)별 표시
- **상품 상세 정보 & 상호작용**
  - 상품 사진, 판매자 매너온도 및 판매 상품 내역 확인
  - 찜하기(관심 목록) 및 실시간 관심 수 반영
  - 조회수 실시간 집계
- **중고거래 글쓰기**
  - 다중 이미지 업로드 및 미리보기
  - 가격 및 나눔 설정, 상세 설명 작성
- **사용자 인증 & 프로필 (Supabase Auth)**
  - 이메일/비밀번호 회원가입 및 로그인
  - 프로필 관리 및 사용자별 판매 내역 관리
- **반응형 모바일 퍼스트 UI**
  - 모바일 웹앱 및 데스크톱 환경 모두에 최적화된 직관적인 디자인

---

## 🛠 기술 스택

- **Frontend**: HTML5, CSS3, Modern JavaScript (Vanilla JS ES6+)
- **Backend / Database**: [Supabase](https://supabase.com/) (PostgreSQL, Supabase Auth, Realtime)
- **Icons & Styling**: Font Awesome, Custom CSS Grid/Flexbox
- **Deployment**: GitHub Pages / Static Web Hosting

---

## 🚀 빠른 시작 (Local Getting Started)

별도의 복잡한 빌드 과정 없이 정적 파일 호스팅으로 즉시 실행할 수 있습니다.

### 1. 저장소 클론
```bash
git clone https://github.com/<your-username>/gamza.git
cd gamza
```

### 2. 브라우저에서 실행
- `index.html` 파일을 더블 클릭하여 브라우저에서 바로 열거나,
- VS Code의 **Live Server** 확장 프로그램을 사용하여 로컬 서버(예: `http://localhost:5500`)로 실행합니다.

---

## ⚙️ Supabase 설정 안내

이 프로젝트는 Supabase를 데이터베이스 및 사용자 인증 백엔드로 사용합니다.

1. [Supabase](https://supabase.com/)에서 새 프로젝트를 생성합니다.
2. `products`, `profiles`, `product_likes`, `chat_rooms` 등의 테이블을 구성하고 RLS(Row Level Security)를 설정합니다.
3. `index.html` 파일 내의 `SUPABASE_URL`과 `SUPABASE_ANON_KEY`를 본인 프로젝트의 키로 교체합니다.

> ⚠️ **보안 주의사항**:
> 클라이언트(`index.html`)에는 반드시 공개 가능한 **`anon` (공개) 키**만 사용해야 합니다.
> RLS를 우회할 수 있는 **`service_role` 키**나 관리자 액세스 토큰은 절대 클라이언트 코드나 공개 저장소에 포함되어서는 안 됩니다.

---

## 📂 프로젝트 구조

```text
gamza/
├── index.html           # 메인 단일 페이지 웹 애플리케이션 (통합본)
├── screen1_list.html    # 화면 1: 상품 목록 뷰
├── screen2_detail.html  # 화면 2: 상품 상세 뷰
├── screen3_write.html   # 화면 3: 상품 등록 뷰
├── .env.example         # 환경 변수 설정 예시
├── .gitignore           # Git 제외 파일 목록
└── README.md            # 프로젝트 문서
```

---

## 🌐 GitHub Pages 배포 방법

1. GitHub 저장소의 **Settings** 메뉴로 이동합니다.
2. 좌측 메뉴에서 **Pages**를 선택합니다.
3. **Build and deployment** > **Branch**에서 `main` 브랜치 및 `/ (root)` 폴더를 선택하고 **Save**를 누릅니다.
4. 몇 분 후 제공되는 URL (`https://<username>.github.io/gamza/`)을 통해 전 세계 어디서나 웹앱에 접속할 수 있습니다!
