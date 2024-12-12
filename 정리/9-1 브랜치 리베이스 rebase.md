Rebase의 이해
- Base를 재배치하는 rebase 병합
  - rebase는 브랜치의 **기반(base)**을 다른 커밋으로 이동시키는 과정이다.
  
- 3-way 병합과 rebase의 차이
  - 3-way 병합은 두 개의 브랜치와 그들의 공통 조상을 기반으로 병합하는 방식이다.
  - rebase는 브랜치의 커밋을 새로운 기반으로 재배치하여 선형적인 이력을 만든다.

3-way 병합과 Rebase 비교
- 3-way 병합
  - 여러 변경 내용의 이력이 모두 그대로 남아있기 때문에 이력이 복잡해진다.
  
- Rebase
  - 히스토리가 선형으로 단순해지고 좀 더 깨끗한 이력을 남긴다.
  - 원래의 커밋 이력이 변경되므로, 정확한 이력을 남겨야 할 필요가 있을 경우에는 사용하면 안 된다.

브랜치 병합 과정
- 브랜치 병합 개요
  - 브랜치 병합은 두 개의 브랜치를 통합하는 과정이다.
  
- 선형적 통합 rebase 이해
  - rebase를 통해 브랜치의 이력을 선형적으로 유지할 수 있다.

Rebase 수행 방법
- 재배치 rebase 병합 수행
  - `git rebase master` 명령어를 사용하여 base를 수정한다.
  - B에서 마스터의 최신 커밋인 D로 수정하고, D 이후에 bugfix를 배치한다.

- fast-forward 병합
  - 이 병합을 직접 다시 수행해야 하며, 'master' 브랜치의 HEAD가 'bugfix' 브랜치의 마지막 커밋으로 이동한다.

충돌 발생과 해결 절차
- 충돌 발생 가능
  - 이동되는 X와 Y의 내용이 'master'의 C, D 커밋들과 충돌하는 부분이 생길 수 있다.
  
- 해결 절차
  1. 각각의 커밋에서 발생한 충돌 내용을 수정한다.
  2. 수정 후, 파일을 추가하고 `git add <수정파일>` 명령어를 사용한다.
  3. rebase를 계속 수행하며 마지막 메시지를 수정한다: `git rebase --continue`.

3-way 병합과 Rebase 비교
- 3-way 병합
  - `git merge` 명령어를 사용하여 두 브랜치를 병합한다.
  
- Rebase 병합
  - `git rebase <newparent> <branch>` 명령어를 사용하여 선행 브랜치의 최근 커밋 이후에 branch를 배치한다.

Fast-forward 병합과 Rebase
- Fast-forward 병합
  - 조상에 위치한 브랜치에서 선행 브랜치의 마지막으로 이동하는 병합 방식이다.
  
- Rebase
  - 두 갈래의 브랜치에서 기존의 베이스를 수정하여 병합할 브랜치의 마지막 커밋을 새로운 베이스로 수정하는 병합이다.

Rebase의 일반적 방법
- 일반적 rebase 방법
  - topic에서 main을 rebase 한 이후, 다시 main으로 이동하여 fast-forward 병합을 수행한다.
  
- 다른 rebase 방법
  - 어느 브랜치든 main topic 순서로 재배치하는 방법이 있다.

Rebase 수행 실습
- 브랜치 topic에서 수행
  - `git switch topic` 명령어를 사용하여 topic 브랜치로 전환한 후, `git rebase main` 명령어를 실행한다.
  
- 성공적인 rebase
  - "Successfully rebased and updated refs/heads/topic." 메시지가 출력된다.

Rebase 후 Fast-forward 병합
- 브랜치 main에서 브랜치 topic으로 빨리감기
  - `git switch main` 명령어를 사용하여 main 브랜치로 전환한 후, `git merge topic` 명령어를 실행한다.
  
- Fast-forward 병합 결과
  - "Updating f297212..3ef33a8" 메시지가 출력되며, 변경 사항이 main 브랜치에 통합된다.

Rebase 병합 요약
- 기준 브랜치에서 main 브랜치 rebase 병합
  - `git checkout topic` 명령어로 topic 브랜치로 전환한 후, `git merge main` 명령어를 사용하여 다시 main으로 돌아와 fast-forward 병합을 진행한다.
