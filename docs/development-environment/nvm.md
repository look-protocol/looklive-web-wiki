프로젝트에서는 Node.js v20.19.2 (LTS)를 사용하고 있습니다.

개발자들의 Node.js 버전 통일을 위해서는 nvm을 사용하고 있습니다.  
[링크](https://github.com/nvm-sh/nvm?tab=readme-ov-file#install--update-script)에서 nvm을 설치해 주세요.

프로젝트 경로에 있는 .nvmrc 파일로 사용하는 노드 버전을 지정합니다.

``` zsh
nvm install // nvmrc에 있는 node 버전이 설치되어 있지 않을 때
nvm use
```
위의 명령어를 입력하시면 실행되어 있는 터미널에서는 해당 노드 버전으로 전환됩니다.
``` zsh
Found '/Users/puro/projects/gitlab/freecap-web/.nvmrc' with version <v20.19.2>
Now using node v20.19.2 (npm v10.8.2)
```
터미널을 종료하시면 다시 로컬 노드 버전으로 돌아갑니다.