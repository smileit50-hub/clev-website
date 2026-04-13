# CLEV Website - GitHub 업로드 및 도메인 연결 가이드

이 저장소는 클레브(CLEV) 프리미엄 유리창 청소 서비스의 공식 웹사이트 소스 코드입니다. 가비아(Gabia)에서 구매한 도메인을 연결하기 위한 절차는 다음과 같습니다.

## 🚀 GitHub에 파일 올리기

1. GitHub에서 새로운 저장소(Repository)를 생성합니다.
2. 로컬 PC의 `clev-website` 폴더 내의 모든 파일을 선택하여 GitHub 저장소에 업로드합니다.
3. (또는 Git CLI 사용)
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin [저장소 URL]
   git push -u origin main
   ```

## 🌐 도메인 연결하기 (가비아 & Vercel/GitHub Pages)

### 방법 1: Vercel을 사용하는 경우 (권장)
Vercel은 가장 빠르고 쉬운 배포 방법입니다.

1. [Vercel](https://vercel.com/)에 가입 후 GitHub 저장소를 연결합니다.
2. 프로젝트 설정의 **Domains** 메뉴에서 가비아에서 산 도메인을 추가합니다.
3. Vercel에서 제공하는 **DNS 설정값(A 레코드 또는 CNAME)**을 복사합니다.
4. **가비아 DNS 설정**:
   - 가비아 홈페이지 -> My가비아 -> 도메인 관리 -> DNS 설정
   - `@` (호스트)와 Vercel에서 준 IP 주소를 A 레코드로 등록하거나, `www`를 CNAME으로 등록합니다.

### 방법 2: GitHub Pages 직접 사용
1. GitHub 저장소 설정(Settings) -> Pages 메뉴로 이동합니다.
2. **Custom Domain** 섹션에 가비아 도메인을 입력합니다.
3. GitHub에서 안내하는 4개의 A 레코드 IP를 가비아 DNS 설정에 등록합니다.

---

## 🛠️ 수정된 사항
- 모든 이미지 경로가 상대 경로(`./assets/`)로 수정되어 온라인 배포 시 이미지가 정상적으로 표시됩니다.
- 가비아 도메인 연결을 위해 필요한 설정 파일들이 준비되었습니다.
- 홈페이지 하단 저작권 표시 연도를 2023년으로 수정하였습니다.
