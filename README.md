# 수업 자료 웹사이트

## 폴더 구조
```
index.html         학생용 페이지 (목록 + 전체화면 미리보기)
admin.html          관리자용 업로드 페이지
materials/
  index.json        자료 목록 (자동 관리됨, 처음엔 빈 배열)
```

## 설치 방법
1. GitHub에 새 저장소 생성 (Public 권장 — 무료 계정은 Private 저장소에서 Pages를 쓸 수 없습니다)
2. 이 폴더의 파일들을 저장소 루트에 그대로 업로드 (index.html, admin.html, materials/index.json)
3. 저장소 Settings → Pages → Branch를 `main` (또는 사용하는 브랜치)으로 설정 후 저장
4. 몇 분 후 `https://{계정}.github.io/{저장소이름}/` 으로 접속 가능

## PAT(Personal Access Token) 발급
1. GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens
2. 해당 저장소만 선택, Repository permissions에서 **Contents: Read and write** 권한만 부여
3. 만료 기한은 짧게 설정 (예: 30일) 후 필요할 때마다 재발급 권장

## admin.html 사용법
1. `https://{계정}.github.io/{저장소이름}/admin.html` 접속
2. 소유자(계정), 저장소 이름, 브랜치, PAT 입력 (탭을 닫으면 사라짐 — 매번 입력 필요)
3. 제목, 자료 유형 선택 후 등록 → 자동으로 `날짜_시간_제목.확장자` 파일명으로 커밋됨
4. 등록된 자료 목록에서 삭제도 가능

## 학생 접근 제한이 필요한 경우
Public 저장소라 URL을 아는 사람은 누구나 접속할 수 있습니다. 검색엔진 노출만 막고 싶다면
저장소 루트에 아래 내용으로 `robots.txt`를 추가하세요.
```
User-agent: *
Disallow: /
```
