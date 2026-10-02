# 모닥방 페이지

`page.modakbang.com` 에 올라가는 정적 사이트. 앱스토어의 지원 URL·마케팅 URL·개인정보 처리방침 URL과 AdMob `app-ads.txt` 를 모아 둔다.

| 경로 | 쓰임 |
|---|---|
| `/` | 개발자 웹사이트 (App Store 지원 URL 루트 = AdMob 개발자 웹사이트) |
| `/app-ads.txt` | AdMob 판매자 인증 |
| `/chargin/` | 충전 마케팅 URL |
| `/chargin/support/` | 충전 지원 URL |
| `/chargin/privacy/` · `/chargin/terms/` | 처리방침·약관 (앱 안 링크) |
| `/en/...` | 영어판 |

## 커스텀 도메인 연결 (한 번만)

1. 가비아 › DNS 관리 › `modakbang.com` › 레코드 추가: 타입 `CNAME`, 호스트 `page`, 값 `qlqlrh.github.io.`
2. 이 저장소에 `CNAME` 파일(`page.modakbang.com` 한 줄)을 커밋한다.
3. GitHub › Settings › Pages 에서 Enforce HTTPS 를 켠다.

DNS 가 연결되기 전에 2번을 하면 github.io 주소가 아직 없는 도메인으로 넘어가 버린다. 순서를 지킨다.

문서 내용은 충전 앱이 실제로 저장하는 값(`charge/supabase/migrations`) 기준이다. 저장 항목이 바뀌면 처리방침도 같이 고친다.
