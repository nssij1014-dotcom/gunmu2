# 근무표 2 (4조 3교대 근무표 자동화)

근무표 · 시간외근무명세서(1·2) · 시간외근무 통계를 자동 계산하는 앱입니다. 인터넷 없이도 쓸 수 있습니다.
(기존 "순찰 근무표" 앱 저장소 `gunmu`와는 별개입니다.)

| 사용 방법 | 주소 |
|---|---|
| 웹 | https://nssij1014-dotcom.github.io/gunmu2/ |
| 안드로이드 | https://github.com/nssij1014-dotcom/gunmu2/releases/latest/download/gunmu2.apk |
| Windows 설치 프로그램 | https://github.com/nssij1014-dotcom/gunmu2/releases/latest/download/gunmu2-setup.exe |

## 구성
- `engine.js` 계산 엔진(근무표·연장·야간·휴일·주6일·색), `index.html` 화면, `holidays.js` 공휴일 2020~2050
- `test/` 계산 시험 (`node test/engine.test.js`)
- `apk/` 안드로이드(Capacitor), `win/` Windows(Electron) 포장
- `.github/workflows/` main에 올리면 시험 → APK·설치 파일 빌드 → Releases(`app`)에 `gunmu2.apk`, `gunmu2-setup.exe` 교체

## 설정
- 웹: Settings → Pages → Branch `main` / `/ (root)`
- APK 서명 키를 고정하려면 Secrets에 `DEBUG_KEYSTORE_B64` 등록 (없으면 빌드마다 임시 키)
