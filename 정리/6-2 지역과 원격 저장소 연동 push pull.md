비밀번호 인증 대체 방법
- 비밀번호 인증은 2021년 8월 13일 이후로 지원이 중단되었다.
- 사용자는 개인 접근 토큰을 사용해야 하며, 이는 GitHub 계정마다 생성해야 한다.
- 에러 메시지:
  - "Support for password authentication was removed on August 13, 2021."
  - "The requested URL returned error: 403"
- 이러한 변경은 강화된 인증 방법으로, 비밀번호 대신 토큰을 사용하여 접근하도록 요구된다.

개인 접근 토큰 생성 절차
- GitHub.com에 로그인한 후, 우측 메뉴에서 Settings를 선택해야 한다.
- 프로파일 settings 메뉴에서 왼쪽 메뉴의 가장 하단에 있는 Developers settings를 클릭한다.
- Personal access tokens에서 Generate new token을 선택하여 새로운 토큰을 생성한다.
- 생성된 토큰은 잘 보관해야 하며, 후에 토큰이 표시되지 않기 때문에 주의가 필요하다.

원격 저장소 수정 후 Pull
- 깃허브 원격 저장소 수정 후 pull은 지역 저장소에서 원격 저장소의 수정을 반영하는 과정이다.
- Push와 Pull의 개념:
  - Push: 지역 저장소의 변경 사항을 원격 저장소로 전송하는 과정이다.
  - Pull: 원격 저장소의 변경 사항을 지역 저장소로 가져오는 과정이다.
- 일상생활의 비유: 밀기와 끌기, 올리기와 내리기로 설명할 수 있다.

Push와 Pull의 개념
- Push와 Pull은 Git의 기본적인 작업 흐름을 나타낸다.
- Push:
  - 지역 저장소에서 원격 저장소로 코드 변경 이력을 전송하는 명령이다.
  - 명령어 예시: `$ git push <저장소별칭명> <브랜치명>`
- Pull:
  - 원격 저장소의 수정을 지역 저장소에 반영하는 과정이다.
  - 명령어 예시: `$ git pull origin main`

인증 오류 및 해결 방법
- 윈도우에서 Push 중 오류가 발생할 수 있으며, 이는 인증 오류와 관련이 있다.
- 에러 메시지:
  - "remote: Permission to …"
  - "fatal: unable to access 'https://github.com/….git/': The requested URL returned error: 403"
- 해결 방법:
  - PAT(Personal Access Token)를 사용하여 연결해야 한다.
  - 명령어 예시: `$ git push -u https://{token}@github.com/{username}/{repo_name}.git`

지역 저장소에서 Push
- 지역 저장소에서 Push는 원격 저장소로 변경 사항을 전송하는 과정이다.
- 쓰기 권한이 있어야 Push가 가능하며, 자신의 저장소나 다른 사람의 저장소라면 협업자로 등록되어야 한다.
- Push 명령어:
  - `$ git push origin topic`
  - 인자를 생략할 수 있는 방법도 있다.
