# 🏢 직원관리 시스템

> 회원가입 · 관리자 승인 · 연차관리(관리자 전용) 기능이 포함된 직원관리 시스템

---

## 🚀 배포 방법 (GitHub + Netlify)

### 1단계 – GitHub에 업로드

1. [github.com](https://github.com) 로그인 후 **New repository** 클릭
2. 저장소 이름 입력 (예: `employee-management`)
3. `Public` 또는 `Private` 선택 후 **Create repository**
4. 로컬에서 다음 명령 실행:

```bash
git init
git add .
git commit -m "직원관리시스템 초기 배포"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/employee-management.git
git push -u origin main
```

> 또는 GitHub 웹사이트에서 파일을 직접 드래그 앤 드롭으로 업로드할 수 있습니다.

---

### 2단계 – Netlify 연동

1. [netlify.com](https://netlify.com) 로그인 (GitHub 계정으로 로그인 권장)
2. **Add new site** → **Import an existing project** 클릭
3. **GitHub** 선택 후 저장소 권한 허용
4. 배포할 저장소 선택 (`employee-management`)
5. 설정:
   - **Build command**: *(비워두기)*
   - **Publish directory**: `.` (점 하나)
6. **Deploy site** 클릭

배포 완료 후 `https://랜덤이름.netlify.app` 주소로 접근 가능합니다.

---

### 3단계 – 자동 배포 설정 (선택 사항)

GitHub에 파일을 push할 때마다 Netlify가 자동으로 업데이트됩니다.  
별도 설정 없이 GitHub 연동만 되어 있으면 자동으로 작동합니다.

---

## 🔑 초기 관리자 계정

| 항목 | 값 |
|------|-----|
| 아이디 | `admin` |
| 비밀번호 | `admin1234` |

> ⚠️ 첫 로그인 후 **관리자 패널 → 관리자 계정 설정**에서 반드시 비밀번호를 변경하세요!

---

## 📋 주요 기능

| 기능 | 권한 |
|------|------|
| 회원가입 신청 | 누구나 |
| 로그인 | 승인된 회원 |
| 대시보드 | 로그인한 모든 사용자 |
| 직원관리 | 로그인한 모든 사용자 |
| **연차관리** | **관리자 전용** |
| 직무교육 | 로그인한 모든 사용자 |
| 백업관리 | 로그인한 모든 사용자 |
| 회원 승인/거절 | 관리자 전용 |
| 관리자 계정 설정 | 관리자 전용 |

---

## ⚠️ 참고 사항

- 데이터는 브라우저의 **localStorage**에 저장됩니다.
- 다른 기기에서 접속하면 데이터가 공유되지 않습니다.
- 정기적으로 **백업 다운로드** 기능을 이용해 데이터를 보관하세요.
- 완전한 서버 기반 데이터 공유가 필요하다면 Firebase, Supabase 등 백엔드 연동이 필요합니다.

---

## 📁 파일 구조

```
/
├── index.html        ← 직원관리 시스템 메인 파일
├── netlify.toml      ← Netlify 배포 설정
└── README.md         ← 이 파일
```
