# SEMLAB 홈페이지 관리자 가이드

홈페이지 주소: https://ims999916-dot.github.io/SEMlab/
관리자 패널: https://ims999916-dot.github.io/SEMlab/admin/

---

## 1. 관리자 패널 (Decap CMS) 로그인

1. https://ims999916-dot.github.io/SEMlab/admin/ 접속
2. "Login with GitHub" 클릭
3. GitHub 계정으로 로그인

> 멤버에게 CMS 권한 부여하려면:
> GitHub 레포지토리 → Settings → Collaborators → Add people

---

## 2. 소식 / 공지 작성

1. 관리자 패널 → 좌측 "소식 & 공지" 클릭
2. 우측 상단 "새 글 작성" 클릭
3. 제목, 날짜, 카테고리(공지/활동/수상/갤러리/기타) 입력
4. 내용 작성
5. 우측 상단 "Publish" 클릭

> 카테고리를 "갤러리"로 선택하고 이미지를 업로드하면
> Gallery 페이지에도 자동으로 표시됩니다.

---

## 3. 갤러리 사진 올리는 방법

### 방법 A — 관리자 패널 사용 (권장)

1. 관리자 패널 → "소식 & 공지" → "새 글 작성"
2. 카테고리: **갤러리** 선택
3. 제목 입력 (예: "2025 춘계학술대회")
4. 날짜 입력
5. "대표 이미지" 항목에서 사진 업로드
6. Publish

→ Gallery 페이지에 자동 반영 (2~5분 소요)

### 방법 B — GitHub 직접 업로드

1. 레포지토리 → assets/images/gallery 폴더 이동
2. Add file → Upload files
3. 사진 파일 업로드 (파일명 영문 권장, 예: conference-2025.jpg)
4. _posts 폴더에 새 파일 생성:
   파일명 형식: YYYY-MM-DD-제목.md

   파일 내용:
   ---
   title: 2025 춘계학술대회
   date: 2025-04-15
   category: 갤러리
   image: conference-2025.jpg
   ---

5. Commit changes → 2~5분 후 반영

---

## 4. 멤버 추가 / 수정 / 삭제

### 추가
1. 관리자 패널 → "멤버" → "멤버 추가"
2. 이름, 직책, 이메일, 연구분야 입력
3. 프로필 사진 업로드 (선택)
4. 정렬 순서 입력 (숫자 낮을수록 먼저 표시, 교수=1 권장)
5. Publish

### 수정
1. 관리자 패널 → "멤버" → 해당 멤버 클릭
2. 내용 수정 후 Publish

### 삭제
1. 관리자 패널 → "멤버" → 해당 멤버 클릭
2. 우측 상단 "Delete" 클릭

---

## 5. 사진 파일 권장 사항

- 형식: JPG 또는 PNG
- 크기: 1MB 이하 권장 (용량 크면 로딩 느려짐)
- 갤러리 사진 비율: 4:3 권장
- 프로필 사진 비율: 1:1 (정사각형) 권장
- 파일명: 영문+숫자만 사용 (한글 파일명 오류 가능)
  예) profile-홍길동.jpg (X) → profile-hong.jpg (O)

---

## 6. 홈페이지 디자인/구조 수정

코드를 직접 수정할 경우 GitHub에서 해당 파일을 열고 편집:

| 수정 대상 | 파일 위치 |
|----------|----------|
| 메인 페이지 | index.html |
| 공통 네비게이션/푸터 | _layouts/default.html |
| 멤버 페이지 | members/index.html |
| 소식 페이지 | news/index.html |
| 갤러리 페이지 | gallery/index.html |
| 사이트 기본 설정 | _config.yml |

---

## 7. 배포 상태 확인

수정 후 반영까지 보통 2~5분 소요.
레포지토리 → Actions 탭에서 진행 상황 확인 가능.
- 🟡 주황 원: 빌드 중
- ✅ 초록 체크: 완료
- ❌ 빨간 X: 오류 (오류 클릭하면 원인 확인 가능)

---

## 8. 문의

홈페이지 관련 문의: 2568602@pcu.ac.kr
