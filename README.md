# Guitar Trainer 공개 배포

Guitar Trainer의 설치 파일과 배포 안내를 제공하는 저장소입니다.
현재는 macOS 첫 공개 배포를 준비하고 있으며, 설치 파일은 아직 게시하지 않았습니다.

- 배포 안내: <https://3rd-person-team.github.io/guitar-trainer-releases/>
- 릴리스: <https://github.com/3rd-person-team/guitar-trainer-releases/releases>

서명·공증, 설치, 업데이트와 자료 복원 확인을 마친 파일만 릴리스에 게시합니다.
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
