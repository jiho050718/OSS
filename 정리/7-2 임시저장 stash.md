깃 영역과 임시저장
- 깃4 영역과 임시저장 개요에 대한 설명이다.
- 저장소는 `.git` 폴더로 구성되어 있으며, 주요 명령어는 다음과 같다:
  - `add`
  - `commit`
  - `restore`
  - `restore --staged`
  - `stash`
- 깃3 영역과 stash 영역의 관계를 이해하는 것이 중요하다.
- 상태:
  - "Nothing to commit, working tree is clean" 상태를 유지해야 한다.

Git Stash의 정의
- 사전적 의미: stash는 놓다, 남겨두다, 감추다, 안전한 곳에 숨겨두다의 의미를 가진다.
- 기능:
  - 커밋할 필요 없이 파일의 변경사항을 숨기거나 비밀리에 저장할 수 있는 강력한 도구이다.
  - 작업 디렉토리와 스테이징 영역의 원래 내용을 stash 스택에 저장한다.
  - 따로 안전한 곳에 저장했다가 다시 가져올 수 있는 기능을 제공한다.

임시저장 명령어
- 임시저장 명령어는 작업 폴더와 스테이징 영역을 숨김(stash)에 저장하고 작업 폴더를 정리하는 데 사용된다.
- 주요 명령어:
  - `$ git stash`
  - `$ git stash -m '메시지'`
  - `$ git stash save`
  - `$ git stash save '메시지'`
- 옵션:
  1. `--keep-index`, `-k`: 스테이징 영역은 제외하고 작업 폴더만 저장한다.
  2. `--include-untracked`, `-u`: Untracked 파일도 포함해 저장한다.

임시저장 복원 방법
- 복원 명령어:
  - `$ git stash apply`: 기본적으로 작업 디렉토리 내용만 다시 복사해 활용한다.
  - `$ git stash apply --index`: 스테이지 영역도 함께 복사하기 위해 사용된다.
- 목표: 최근 임시 저장 내용을 가져와 반영하고, stash 목록은 그대로 유지한다.

Stash 목록 관리
- 목록 보기:
  - `$ git stash list`: stash 목록을 확인할 수 있다.
  - 예시: `stash@{0}`, `stash@{1}`, `stash@{2}` 등으로 가장 최신 것이 0번이다.
- 특정 stash 확인:
  - `$ git stash show`: 해당 stash 항목이 생성되었을 때의 커밋 자료와 최신 stash 항목 간의 차이를 표시한다.
  - `$ git stash show -p`: 변화된 파일과 변화된 수를 표시한다.

특정 Stash 확인 및 삭제
- 삭제 명령어:
  - `$ git stash drop`: 지정된 임시 저장 내용을 삭제한다.
  - `$ git stash clear`: 모든 stash 목록을 제거한다.
- 최근 임시 저장 내용을 삭제하는 방법을 배운다.

Untracked 파일 관리
- Untracked 파일 삭제:
  - `$ git clean`: Untracked 파일을 삭제하는 명령어이다.
  - 경고 메시지: "fatal: clean.requireForce defaults to true and neither -i, -n, nor -f given; refusing to clean"와 같은 경고가 발생할 수 있다.
- 옵션:
  - `$ git clean -i`: 인터랙티브 모드로 삭제할 파일을 선택할 수 있다.
  - `$ git clean -f`: 강제로 삭제하는 명령어이다.

요약 및 결론
- 작업 디렉토리와 스테이징 영역을 숨김(stash)에 저장하고 작업 폴더를 정리하는 것이 핵심이다.
- 주요 명령어:
  - `$ git stash`
  - `$ git stash -m '메시지'`
  - `$ git stash save`
- 복원 명령어:
  - `$ git stash pop`: 최근 또는 지정된 임시 저장소 내용을 가져와 반영하고 삭제한다.
  - `$ git stash apply`: 작업 디렉토리와 스테이징 영역도 반영한다.
- 목록 관리:
  - `$ git stash list`: stash 목록을 확인하고 관리한다.
