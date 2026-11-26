# Guitar Trainer macOS 파일럿

첫 일반 앱 파일럿 **0.1.4 beta**를 제공합니다. Apple Silicon(M1 이상), macOS 27.2 이상이 대상입니다.

- [소개 페이지](https://3rd-person-team.github.io/guitar-trainer-releases/) (Mac App Store 출시 예정 안내. 파일럿 설치 파일은 아래 릴리스에 있습니다.)
- [0.1.4 릴리스와 설치 안내](https://github.com/3rd-person-team/guitar-trainer-releases/releases/tag/v0.1.4)

로컬 악보·연습·기록·백업을 사용할 수 있으며 이번 빌드에는 로그인 서버를 연결하지 않았습니다.
기존 앱을 사용했다면 먼저 전체 자료를 백업하세요. 개발 서버와 설치 앱의 자료는 자동 이관되지 않습니다.

`qa-upgrade-v*`와 `qa-upgrade/`는 별도 앱의 업그레이드 검증용이며 일반 설치용이 아닙니다.
운영 beta manifest는 `channels/beta/latest.json`, 서명된 정책은
`channels/beta/darwin-aarch64/policy.json`에 있습니다. revision 1은 최신 0.1.4를 안내하며
최소 버전 0.1.0을 유지해 기존 버전을 강제로 차단하지 않습니다.

Intel Mac, Windows, 모바일과 장치별 장시간 동작은 이번 검증 범위에 포함되지 않습니다.
구체적인 알려진 제한, 검증 범위, SHA-256은 해당 릴리스를 확인하세요.

## 별도 업그레이드 QA

`qa-upgrade-v0.1.x` 사전 배포는 실제 설치·업그레이드·자료 보존을 확인하는
**Guitar Trainer Upgrade QA** 앱입니다. 일반 앱과 bundle ID, 영속 WebKit 저장소,
업데이트 주소를 분리합니다. macOS Apple Silicon / macOS 27.2 검증용이며 일반 사용자용
배포 또는 다른 OS 지원을 뜻하지 않습니다.

현재 [QA 0.1.3](https://github.com/3rd-person-team/guitar-trainer-releases/releases/tag/qa-upgrade-v0.1.3)은
실제 0.1.2→0.1.3 필수 업데이트 설치·새 프로세스 자동 시작과 자료 보존 검증을 완료했습니다.
연습 중 수동 정책 확인 후 자동 종료·저장을 거쳤으며, 설치 전후와 완전 종료·재실행 후
이벤트 40개를 포함한 10개 저장소의 모든 필드·바이너리와 원본 영상 2개의 재내보내기가 일치했습니다.
실제 입력 장치 녹화, 물리 절전·네트워크 단절/재연결, Windows 및 일반 운영 배포는 검증 범위 밖입니다.

서명·공증된 실제 QA 바이너리만 게시하며, 해당 릴리스에 정확한 검증 상태를 기록합니다.
QA manifest는 `qa-upgrade/channels/beta/latest.json`, 서명 정책은
`qa-upgrade/channels/beta/darwin-aarch64/policy.json`을 사용합니다. 운영 `channels/`
경로와 운영 release tag는 QA 작업에서 변경하지 않습니다.
