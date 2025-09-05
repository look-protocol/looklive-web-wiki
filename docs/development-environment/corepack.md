# pnpm 버전 관리

> 현재 사용중인 pnpm 버전은 10.12.1입니다.

pnpm의 버전 관리는 Corepack을 사용합니다.
Corepack을 사용해 pnpm을 설치해 주세요

1. Corepack을 설치합니다.
``` zsh
npm install --global corepack@latest
```
2. pnpm을 설치합니다.
``` zsh
corepack enable pnpm
```

pnpm이 Corepack을 통해 설치되어 있으면 자동으로 package.json에 명시되어 있는 버전으로 고정됩니다.

다른 버전 사용이 필요하다면 아래와 같은 형식의 명령어를 사용합니다.
``` zsh
corepack use pnpm@latest-10
```