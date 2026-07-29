# 🎢 롤러코스터 타이쿤 수학 퀴즈 (Rollercoaster Tycoon Math Quiz)

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Database: Supabase](https://img.shields.io/badge/Database-Supabase-3ECF8E.svg)
![Deployment: Vercel](https://img.shields.io/badge/Deployment-Vercel-000000.svg)

초등학교 수학 문제를 풀며 나만의 놀이공원을 건설하는 롤러코스터 타이쿤 웹앱입니다.  
**Supabase 클라우드 데이터베이스**와 **Vercel** 배포를 완벽하게 지원합니다.

---

## ✨ 주요 기능

1. **🎮 게임 진행 상황 클라우드 저장 / 불러오기 (Supabase & IndexedDB)**:
   - 닉네임과 비밀번호로 학생별 놀이공원 배치 상태, 자금, 가치, 풀이 현황을 Supabase 클라우드 DB에 안전하게 저장 및 복원.
   - DB 미설정 시 브라우저 로컬 IndexedDB 자동 전환 지원.

2. **📝 단원별 퀴즈 & 주관식/객관식 문제 지원**:
   - 3학년 1학기 5단원 "길이와 시간" 등 원하는 수학 단원을 선택하여 풀이.
   - 객관식(4지 선다) 및 주관식(텍스트 정답) 지원.

3. **👩‍🏫 교사 대시보드 (CSV 업로드/다운로드)**:
   - 엑셀 편집용 `MATH_QUIZ_TEMPLATE.csv` 기본 양식 다운로드 제공.
   - 교사가 새로 만든 단원 및 문제를 CSV 파일로 업로드하여 DB에 일괄 등록.

---

## 🚀 1. GitHub 업로드 방법

터미널에서 아래 명령어로 프로젝트를 GitHub 레포지토리에 푸시(Push)하세요.

```bash
# 1. Git 저장소 초기화 및 브랜치 설정
git init
git branch -M main

# 2. 파일 스테이징 및 커밋
git add .
git commit -m "Feat: Rollercoaster Tycoon Math Quiz with Supabase & Vercel readiness"

# 3. 본인의 GitHub 레포지토리 연결 및 푸시
git remote add origin https://github.com/사용자이름/rollercoaster-math-quiz.git
git push -u origin main
```

---

## ⚡ 2. Supabase 데이터베이스 설정 가이드

1. [Supabase 공식 홈페이지](https://supabase.com)에 로그인 후 새 프로젝트를 생성합니다.
2. 프로젝트 대시보드 좌측 메뉴의 **SQL Editor**로 이동합니다.
3. 이 프로젝트의 `schema.sql` 파일 내용을 복사하여 SQL Editor에 붙여넣고 **[Run]**을 눌러 실행합니다.
   - `game_saves` (게임 저장 테이블) 및 `quiz_questions` (문제 테이블)이 자동 생성됩니다.
4. Supabase **Project Settings -> API** 메뉴에서 **Project URL**과 **anon public key**를 확인합니다.

---

## 🌐 3. Vercel 배포 가이드

1. [Vercel 공식 홈페이지](https://vercel.com)에 접속 후 GitHub 계정으로 로그인합니다.
2. **Add New... -> Project**를 클릭하고 방금 푸시한 `rollercoaster-math-quiz` 저장소를 선택(Import)합니다.
3. **Environment Variables** (환경 변수) 설정에 아래 두 값을 등록합니다:
   - `SUPABASE_URL`: Supabase Project URL (`https://your-project.supabase.co`)
   - `SUPABASE_ANON_KEY`: Supabase anon public key
4. **Deploy** 버튼을 누르면 배포가 완료되며 무료 호스팅 URL이 제공됩니다!

---

## 🛠️ 개발 및 웹 UI 내 DB 설정

웹앱 실행 후 **'👩‍🏫 교사 대시보드'** 모달에서도 Supabase URL과 Key를 직접 입력하여 즉시 연결을 테스트할 수 있습니다.

```bash
# 로컬 개발 서버 실행
npm run dev
```

---

## 📄 라이선스
MIT License
