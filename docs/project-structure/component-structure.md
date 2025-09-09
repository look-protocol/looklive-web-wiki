# 컴포넌트 구조

## 아토믹 디자인

looklive-web 프로젝트 내부의 모든 컴포넌트는 아토믹 디자인을 따릅니다.
(아직은 분류되지 않은 컴포넌트가 존재하지만 곧 수정할 예정입니다.)

[기본적인 아토믹 디자인에 대한 설명](https://tech.kakaoent.com/front-end/2022/220505-how-page-part-use-atomic-design-system/)

## 폴더 구조

src/components 내부에 `atoms`, `molecules`, `organisms`, `templates` 폴더에 각각의 컴포넌트들을 정리하고
pages의 경우에는 src/app 디렉토리 내부에 있는 page.tsx를 아토믹 디자인에서의 pages로 취급합니다.

Atoms를 제외한 모든 컴포넌트는 컴포넌트의 이름과 같은 폴더를 가지고 있고, 그 폴더 내부에는 컴포넌트와 선택적인 story 파일을 가집니다.
* Atoms는 컴포넌트 이름 대신 컴포넌트의 타입(button, text 등)으로 폴더를 생성합니다.

* 현재는 src/components/atomic 이라는 계층 내부에서 관리하고 있지만 추후 상위로 이동할 예정입니다.

## 분류 방법

### Atom

1. 더 이상 분해할 수 없는 기본 컴포넌트는 atom으로 취급합니다.

### Molecule

1. 여러 개의 atom을 결합된 형태입니다.
2. 한 가지 이상의 기능적 역할을 가지고 있습니다.
3. SRP에 따라 1가지의 책임을 집니다.

### Organism

1. organism은 atom, molecule, organism으로 구성할 수 있습니다.
2. atom, molecule에 비해 좀 더 구체적으로 표현되고 컨텍스트를 가지기 때문에 상대적으로 재사용성이 낮습니다.

### Template

1. template는 page를 만들 수 있도록 여러 개의 organism, molecule로 구성할 수 있습니다.
2. 실제 컴포넌트를 레이아웃에 배치하고 구조를 잡는 와이어 프레임입니다. 즉 실제 콘텐츠가 없는 page 수준의 스켈레톤입니다.

### Page

1. 유저가 볼 수 있는 실제 콘텐츠를 담고 있습니다.
2. template의 인스턴스라고 할 수 있습니다.

## 그 외에

- 아토믹 디자인의 각 단계는 선형 프로세스가 아닙니다. 꼭 단계를 따라서 page를 구성할 필요는 없습니다.
- 팀원 개개인에 따라 컴포넌트를 분리하는 기준이 주관적일 수 있습니다. 이러한 부분은 팀원들간의 의논을 통해 좁혀나가야 합니다.
