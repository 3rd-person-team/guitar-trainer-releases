# Guitar Trainer 공개 배포

Guitar Trainer의 설치 파일과 배포 안내를 제공하는 저장소입니다.
현재는 macOS 첫 일반 사용자용 배포를 준비하고 있습니다. 아래 QA 사전 배포는 실제
업그레이드 검증을 위한 별도 앱입니다.

- 배포 안내: <https://3rd-person-team.github.io/guitar-trainer-releases/>
- 릴리스: <https://github.com/3rd-person-team/guitar-trainer-releases/releases>

일반 사용자용 릴리스는 서명·공증, 설치, 업데이트와 자료 복원 확인을 마친 뒤 게시합니다.
공개 후에는 해당 릴리스의 지원 환경과 설치 안내를 먼저 확인해 주세요.

## 업데이트 주소

다음은 게시 예정 경로입니다. 현재 존재하는 다운로드 또는 정책 파일을 뜻하지 않습니다.

| 용도 | Pages 사이트 기준 경로 |
| --- | --- |
| macOS 베타 업데이트 manifest | `channels/beta/latest.json` |
| 채널·OS·CPU별 서명된 지원 정책 | `channels/{channel}/{platform}-{arch}/policy.json` |
| macOS Apple Silicon 베타 정책 | `channels/beta/darwin-aarch64/policy.json` |

설치 파일이 검증되어 공개되기 전에는 위 경로에 임시 manifest나 모의 정책 JSON을 게시하지
않습니다. 실제 정책은 인증 없이 HTTPS로 직접 읽을 수 있어야 하며, 리디렉션 없이 CORS와
캐시 재검증을 지원하는지 게시 시 확인합니다. 설치 파일은 릴리스의 버전별 경로에 보관합니다.

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
경로와 운영 release tag는 변경하지 않습니다.
