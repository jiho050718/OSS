원격 저장소 생성 및 복제
- 원격 저장소 생성:
  - GitHub에서 원격 저장소를 생성할 수 있다.
  - 저장소 이름은 git-clone으로 설정한다.
  
- 복제 명령어:
  - `$ git clone [복사된-주소]` 명령어를 사용하여 원격 저장소를 지역 저장소에 복제한다.
  - 원격 저장소와 동일한 이름으로 복제할 수 있다.

Vscode로 원격 저장소 복제
- Vscode에서의 복제:
  - Vscode를 통해 원격 저장소를 복제하는 방법을 배운다.
  - 복제할 원격 저장소의 주소를 복사한 후, Vscode에서 명령어를 실행한다.

- 명령어 예시:
  - `$ git clone [복사된-주소] [새로운-폴더명]`을 사용하여 특정 폴더에 복제할 수 있다.
  - `$ git clone [복사된-주소] .` 명령어로 현재 폴더에 바로 복제할 수 있다.

원격 저장소 클론 개념
- 클론 개념:
  - 원격 저장소를 지역 저장소에 복제하는 과정을 클론이라고 한다.
  - 공개된 저장소는 소유와 관계없이 누구나 접근할 수 있다.

- 주요 원격 저장소:
  - GitHub(github.com)
  - Bitbucket(bitbucket.org)

원격 저장소 주소 복사
- 주소 복사 방법:
  - GitHub에서 저장소 주소를 복사하는 방법을 설명한다.
  - Code 클릭 후, HTTPS 주소를 복사한다.

- 복사된 주소 사용:
  - 복사된 주소를 사용하여 지역 저장소에 복제 명령어를 실행한다.
  - 예시: `$ git clone https://github.com/ai7dnn/git-clone.git`

복제 명령어 실행
- 복제 명령어:
  - `$ git clone 저장소주소[저장소폴더명]` 명령어를 사용하여 지역 저장소에 복사한다.
  
- 복사 확인:
  - 복사된 폴더를 확인하여 복제 성공 여부를 점검한다.
  - 예시: `Cloning into 'git-clone'...` 메시지가 나타나면 복제 성공이다.

원격 저장소 이름 관리
- 원격 저장소 별칭 관리:
  - `$ git remote` 명령어로 원격 저장소 목록을 확인한다.
  - 기본 이름 origin이 설정된다.

- 별칭 추가 및 수정:
  - `$ git remote add origin URL` 명령어로 원격 저장소 별칭을 추가한다.
  - `$ git remote rename origin org` 명령어로 이름을 수정할 수 있다.
  - `$ git remote rm org` 명령어로 별칭을 삭제할 수 있다.

유명 오픈소스 소프트웨어 복제
- 유명 OSS 목록:
  - GitHub에서 유명한 오픈소스 소프트웨어의 주소를 제공한다.
  - 예시:
    - Vscode: `https://github.com/microsoft/vscode`
    - Atom: `https://github.com/atom/atom`
    - Git: `https://github.com/git/git`
    - TensorFlow: `https://github.com/tensorflow/tensorflow`

- 복제 시 주의사항:
  - 네트워크가 느릴 경우 복제가 어려울 수 있다.
  - 적절한 폴더를 생성하여 복제 작업을 진행한다.

Vscode에서 복제 실행
- Vscode에서의 복제:
  - Vscode를 열고 적당한 폴더를 생성한 후, 복제 작업을 진행한다.
  
- 복제 성공 확인:
  - 복제 성공 후, 복제된 파일을 확인하여 작업이 완료되었는지 점검한다.

원격 저장소 관리 요약
- 원격 저장소 생성 및 관리:
  - GitHub에 원격 저장소를 생성하고, 이를 관리하는 방법을 요약한다.
  
- 주요 명령어:
  - `$ git clone https://github.com/atom/atom.git` 명령어로 원격 저장소를 복제한다.
  - `$ git remote -v` 명령어로 원격 저장소 목록을 확인한다.
  - `$ git remote show origin` 명령어로 원격 저장소의 상세 정보를 확인한다.
