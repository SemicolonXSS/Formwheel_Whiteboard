# Formwheel Whiteboard 🎨

친구들과 실시간으로 함께 그리는 Formwheel 프로젝트입니다.

## 실행

- https://semicolonxss.github.io/Formwheel_Whiteboard/ (GitHub Pages 활성화 필요)
- **새 방 만들기** → **초대 링크 복사** → 친구가 접속해 그림 그리기
- 펜/지우개/직선/사각형/타원, 색상·두께, 방장 전체 지우기, 내 마지막 작업 취소, PNG 저장 지원
- Firebase Authentication의 **Anonymous(익명)** 로그인 방식이 활성화되어 있어야 합니다.
- Firebase Realtime Database에서 `whiteboardRooms` 경로를 위한 보안 규칙이 필요합니다. `database.rules.example.json`은 **화이트보드 경로만을 설명하는 예시**입니다. 기존 데이터베이스 Rules 전체를 덮어쓰지 마세요. 기존 최상위 `rules`에 `whiteboardRooms` 부분을 병합하고 검토하세요.
- 데이터가 DB에 저장되므로 그림은 새로고침 뒤에도 남아 있습니다. 중요한 그림은 PNG로 다운로드하세요.

## 보안 및 제한

기본 URL의 방 코드는 초대용 식별자이지 암호가 아닙니다. 코드를 아는 사람은 방에 접근할 수 있습니다. 민감한 개인정보를 그리거나 공유하지 마세요.
예시 규칙을 실제 DB에 적용하는 작업은 별도로 필요하며, 저장 용량·대규모 동시 접속 제한도 별도로 관리해야 합니다. 프로젝트는 1200×750 캔버스 기준입니다.
