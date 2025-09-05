코드를 검사하는 스크립트들이 기본적으로 package.json에 정의되어 있습니다.

``` typescript
    "format:check": "biome format .",
    "format:fix": "biome format --write .",
    "lint:check": "biome check .",
    "lint:fix": "biome check --write .",
    "type:check": "tsc --noEmit"
```
+ format:check : biome에서 포매팅을 '체크'만 합니다.
+ format:fix : biome에서 포매팅을 '수정'까지 합니다.
+ lint:check : biome에서 린트 관련 에러를 '체크'만 합니다.
+ lint:fix : biome에서 린트 관련 에러를 '수정'까지 합니다.
+ type:check : tsc에서 타입 에러를 '체크'만 합니다.

+ format:fix 명령어는 자유롭게 사용하셔도 지장이 없습니다.
+ lint:fix 명령어는 check만 사용하고 직접 수정을 하시거나 fix되는 소스들에 대한 확인이 필요합니다.
+ type:check에서 체크되는 에러가 있으면 빌드가 되지 않습니다. 직접 수정해 주셔야 합니다.