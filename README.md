# Streaming Card Maker v30 — public deployment build

공개 GitHub Pages 배포를 기준으로 안정성 점검한 버전.

## 점검/개선
- 사용자 입력이나 업로드 이미지를 서버/GitHub/localStorage에 저장하지 않음
- 여러 사용자가 같은 주소에서 동시에 사용해도 각 브라우저 탭 안에서만 상태가 유지됨
- 40MB 초과 이미지 업로드 방지
- 매우 큰 이미지는 브라우저 메모리 문제를 줄이기 위해 자동 축소
- 투명 로고는 PNG 투명도 유지
- PNG 저장 시 data URL 대신 Blob을 사용해 메모리 사용량 완화
- 웹폰트 로딩이 늦어도 최대 3초 뒤 저장을 계속 진행
- html2canvas CDN 1차 로딩 실패 시 보조 CDN으로 자동 재시도
- GitHub Pages 하위 경로에서도 동작하도록 절대 경로 의존성 없음
- 모바일 Pointer Events 기반 드래그 유지

## 배포
저장소 루트의 `index.html`을 이 버전으로 교체하고 GitHub Pages에서 배포하면 돼.
