reset 명령과 옵션
- reset 명령은 Git에서 버전을 되돌리는 데 사용된다.
- 옵션:
  - --hard: 모든 변경 사항을 삭제하고 이전 커밋으로 돌아간다.
  - --mixed: 스테이징 영역과 깃 저장소는 수정되지만, 작업 디렉토리는 유지된다.
  - --soft: 깃 저장소만 수정되며, 작업 디렉토리와 스테이징 영역은 그대로 유지된다.

reset의 기능 이해
- 기능:
  - 특정 커밋으로 완전히 되돌아가는 방법을 제공한다.
  - 타임머신과 같은 개념으로, 이전 상태로 돌아갈 수 있다.
- 주의 사항:
  - reset을 수행하면 해당 커밋 이후의 이력은 모두 사라지므로 주의가 필요하다.
  - 새로운 커밋이 생성되지 않으며, 깃 저장소는 이전 커밋 내용으로 수정된다.

reset 옵션 설명
- reset 옵션:
  - --hard: 작업 디렉토리와 스테이징 영역, 깃 저장소를 모두 이전 커밋의 내용으로 복사 및 수정한다.
  - --mixed: 스테이징 영역과 깃 저장소를 수정하지만, 작업 디렉토리는 이전 내용 그대로 남는다.
  - --soft: 깃 저장소에만 복사 및 수정하며, 작업 디렉토리와 스테이징 영역은 이전 내용 그대로 남는다.

각 옵션의 작동 방식
- 주요 명령:
  1. `$ git reset --hard HEAD~2`: HEAD의 두 번째 이전 커밋으로 모든 내용을 복사 및 수정한다.
  2. `$ git reset --mixed HEAD~`: 스테이징 영역과 깃 저장소를 수정하되, 작업 디렉토리는 그대로 유지한다.
  3. `$ git reset --soft HEAD~`: 깃 저장소에만 복사 및 수정하며, 작업 디렉토리와 스테이징 영역은 이전 내용 그대로 남는다.

reset과 checkout 비교
- reset:
  - 특정 커밋으로 돌아가는 명령이다.
  - `$ git reset <옵션> <커밋ID>` 형식으로 사용된다.
- checkout:
  - HEAD 포인터를 특정 커밋으로 이동하는 명령이다.
  - `$ git checkout <커밋ID>` 형식으로 사용된다.
- 비교:
  - reset은 커밋을 수정하는 반면, checkout은 포인터를 이동하는 방식이다.

reset 후 상태 복원
- 이전 상태로 되돌아가기:
  - `ORIG_HEAD`를 이용하면 매우 간단하게 이전 커밋으로 돌아갈 수 있다.
  - `$ git reset --hard ORIG_HEAD` 명령을 사용하여 바로 이전 커밋으로 복원할 수 있다.

요약 및 결론
- reset 명령 요약:
  - `$ git reset --hard HEAD~2`: HEAD의 두 번째 이전 커밋으로 작업 디렉토리와 스테이징 영역, 깃 저장소에 복사한다.
  - `$ git reset --mixed HEAD~2`: HEAD의 두 번째 이전 커밋으로 스테이징 영역과 깃 저장소에 복사한다.
  - `$ git reset --soft HEAD~2`: HEAD의 두 번째 이전 커밋으로 깃 저장소에만 복사한다.
- reset 취소:
  - 이전에 수행한 reset을 취소하는 명령은 `$ git reset --hard ORIG_HEAD`이다.
