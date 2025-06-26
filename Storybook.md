컴포넌트의 UI나 간단한 기능에 대한 테스트는 Storybook에서 진행합니다.
> Every piece of UI is now a component. The superpower of components is that you don't need to spin up the whole app just to see how they render. You can render a specific variation in isolation by passing in props, mocking data, or faking events.

Storybook Docs의 [get-started 페이지](https://storybook.js.org/docs/get-started/why-storybook)에는 storybook에 대한 내용들이 잘 설명되어 있습니다.

현재 상태에서는 stories 파일은 원본 컴포넌트 파일과 같은 위치에 작성합니다. 직접 stories 파일을 작성하셔도 되지만 storybook의 ui를 이용하셔도 됩니다.

먼저 storybook 서버를 실행합니다.
``` zsh
pnpm storybook
```
localhost:6006으로 접속하신 다음 좌측 상단에서 + 버튼을 클릭하여 스토리를 추가합니다.
![image](uploads/5c0ea5da335253a2589552791a98c0ef/image.png)  
스토리를 작성할 컴포넌트를 검색합니다.
![image](uploads/e8c8d0fe2626e175041d359839ab35e1/image.png)  
클릭하시면 추가가 완료됩니다. 세부적인 설정이 필요한 컴포넌트의 경우네는 하단에서 추가 설정을 진행합니다.  
![image](uploads/cf1a383392721ff226adf30d211e77d8/image.png)  
변경 사항 작성 후 save 버튼을 누르시면 임시적으로 반영되고 Update story 버튼을 누르시면 실제 stories 파일에도 반영됩니다.
