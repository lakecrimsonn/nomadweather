# 날씨앱

<aside>
😆 배움은 언제나 즐거워

# 2.0 snack

- 엑스포의 스낵은 vscode나 node.js가 설치되지 않을 경우, 아이패드나 핸드폰을 이용해서 앱을 만들 수 있다.
- [https://snack.expo.dev](https://snack.expo.dev/)

# 2.1 the rules of native

- view는 컨테이너다.
- 모든 텍스트는 text 컴포넌트에 써야한다. p, span과 같은 태그는 없다.
- StyleSheet.create()은 꼭 필요하지 않다. 태그에 직접 스타일을 넣을 수 있다. 하지만 자동완성을 제공해줘서 편리하다.
- StatusBar는 핸드폰 상단에 시간, 와이파이, 배터리 표시창을 의미한다. “light”로 변경할 시 상태창이 사라진다.

# 2.2 react native packages

- react native docs를 확인하면, 안드로이드에서만 사용할 수 있는 컴포넌트가 있고, ios만 사용할 수 있는 컴포넌트가 있다.
- 개발팀은 과거에 최대한 많은 기능을 제공했으나, 버그가 많아서 이제는 api를 많이 줄였다.

# 2.3 third party packages

- React Native Directory는 서드파티 패키지를 확인해 볼 수 있다. https://reactnative.directory/
- expo sdk는 수많은 api와 컴포넌트가 있다. react native directory에서 패키지를 찾아볼 수 없다면 expo docs를 확인하면 된다. https://docs.expo.dev/versions/latest/
- StatusBar는 expo 버전이 있고, native 버전이 있다. 스테이터스바 뿐만 아니라 커뮤니티 버전의 api와 컴포넌트는 많다. 참고로 스테이터스바는 지워도 사라지지 않는다.

# 2.4 layout system

- 웹에서는 display:flex, flex-direction은 설정할 수 있었다. View태그의 flexDirection은 기본적으로 이미 flex container다. display:flex를 설정하지 않아도 된다. flex-direction 역시 반대반향으로 설정되어 있다. 앱에서는 컬럼이 디폴트.
- 너비와 높이를 이용해서 레이아웃을 디자인 하지 않는다. 아이폰과 안드로이드의 100px은 서로 다르다. 또 반응형으로 만들어야 하기 때문이다. flex를 이용한다. 틸색상의 뷰태그는 다른 요소보다 3배 더 많은 영역을 차지 한다.
- 부모 요소의 flex 설정이 사라지면, 다른 요소 역시 적용되지 않는다.

```jsx
import React from "react";
import { View } from "react-native";

export default function App() {
  return (
    <View style={{ flex: 1, flexDirection: "row" }}>
      <View style={{ flex: 1, backgroundColor: "tomato" }}></View>
      <View style={{ flex: 3, backgroundColor: "teal" }}></View>
      <View style={{ flex: 1, backgroundColor: "orange" }}></View>
    </View>
  );
}
```

</aside>
