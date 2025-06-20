팀 내부에서는 CHANGELOG를 자동 생성하고 팀 동료에게 좀 더 구조화된 커밋 히스토리를 보여주기 위해 기본적으로 AngularJS commit convention을 기반으로 하는 스펙인 Conventional Commits를 따릅니다.  
[영어 버전 문서](https://www.conventionalcommits.org/en/v1.0.0/)  
[한글 버전 문서](https://www.conventionalcommits.org/ko/v1.0.0/)

커밋 메시지는 다음과 같은 구조가 되어야 합니다.
``` text
<타입>[적용 범위(선택 사항)]: <설명>

[본문(선택 사항)]

[꼬리말(선택 사항)]
```

## Commit 타입
+ `build`: 빌드 시스템이나 외부 종속성에 영향을 미치는 변경 사항(예시 : pnpm)
+ `chore`: 소스 또는 테스트 파일을 수정하지 않는 기타 변경 사항
+ `ci`: CI 구성 파일 및 스크립트 추가, 변경
+ `docs`: 문서 관련 수정
+ `feat`: 새로운 기능의 추가, 기존 기능을 수정(FE의 경우 UI에 대한 변경도 기능의 수정으로 취급합니다.)
+ `fix`: 버그 수정
+ `perf`: 성능 향상을 위한 코드 변경
+ `refactor`: 기능의 변화가 없는 코드 리팩터링
+ `revert`: 이전 커밋을 되돌림
+ `style`: 코드의 의미에 영향을 미치지 않는 변경 사항(공백, 서식, 세미클론 누락 등)
+ `test`: 테스트 코드 추가, 기존 테스트 코드 변경
