# 공통 명령 원칙

게임 클라이언트가 제공하는 capabilities를 명령과 매개변수의 최종 기준으로 사용합니다. 명령 이름이나 아이템 이름을 추측하지 않습니다.

주요 흐름:

- 연결 확인: `status`
- 명령 조회: `capabilities`
- 위치·하우징 확인: `get_current_environment`
- 활동 상태 확인: `get_activity`
- 인벤토리 확인: `get_items`
- 채집 항목 조회: `get_gatherable_items`
- 채집 실행: `execute_gathering`
- 진행 중인 중지 가능한 작업 중지: `stop_action`

한국어 등 ASCII가 아닌 요청 본문은 UTF-8 전체 JSON을 base64로 인코딩해 `base64:<값>` 형식으로 전달합니다.
