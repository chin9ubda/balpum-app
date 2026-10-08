# balpum-app

발품(balpum) 앱의 공개 정적 파일을 두는 저장소입니다. GitHub Pages로 배포됩니다.

## update.json — 강제 업데이트 설정

앱(Android store 빌드)이 시작할 때 `https://chin9ubda.github.io/balpum-app/update.json` 을 읽습니다.

- `android.<applicationId>.minVersionCode`: 이보다 낮은 versionCode 를 쓰는 사용자는 앱 사용이 막히고 업데이트로 안내됩니다.
- `android.<applicationId>.message`: 차단 화면에 보일 안내 문구(비우면 앱 기본 문구).

평소 업데이트에는 값을 바꾸지 않습니다(Play 자동 업데이트에 맡김).
광고판 전환처럼 모든 사용자를 새 버전으로 옮겨야 할 때만, 그 버전이 Play 에 배포된 **뒤에** `minVersionCode` 를 올립니다.
배포 전에 올리면 업데이트할 버전이 없어 사용자가 앱을 못 씁니다.
