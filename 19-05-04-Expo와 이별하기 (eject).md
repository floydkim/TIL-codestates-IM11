# EXPO와 이별하기
React-Native를 이용해 모바일 앱을 만들 때, EXPO는 개발자가 앱 코딩을 빨리 시작할 수 있도록 도와줍니다.
Xcode나 Android 프로젝트를 만들고, 프로젝트를 세팅하는 번거로움 없이 바로 코딩을 시작할 수 있게 해주는 유용한 툴입니다.

그런데 EXPO는 네이티브 언어로 된 라이브러리를 이용할 수 없다는 한계가 있습니다. React-Native는 할 수 있는데 EXPO는 안됩니다.
그래서 EXPO를 이용해 앱 개발을 하다 보면 `$ expo eject` 명령을 통해 EXPO와 이별할 수 밖에 없게 됩니다.

EXPO는 React-Native와 어떻게 다르길래 안되는걸까요?

## EXPO의 동작 환경

![expo 동작 환경](https://lh3.googleusercontent.com/uI0fYPxqo0urSM60u_FbYdGwJmSspF5odKhn-RQAQufCtbJG5j9aFxuPqJ_6SXcFgCfBl2IfWVw)

우선 어떤 구조로 EXPO가 동작하는지 살펴보겠습니다.

EXPO는 로컬 개발환경에 두개의 서버를 띄워 동작합니다.
EXPO 모바일 클라이언트에 react-native가 번들링 한 JavaScript 파일을 내려주기 위한 서버(초록색),
EXPO-CLI와 expo 모바일 클라이언트 둘 사이의 통신을 위한 서버(핑크색)을 하나 띄웁니다.

이 중 핵심은 엑스포 클라이언트입니다.
작성한 코드가 모바일 네이티브 환경에서 직접 구동되는것이 아니고, 받아온 앱을 엑스포 클라이언트 안에서 실행시킵니다.

EXPO 공식문서를 통해 위 사실을 알 수 있었습니다.
> EXPO 안에 들어가는 앱은 순수 JavaScript로 작성되고, 절대로 네이티브 iOS나 Android 레이어까지 내려가지 않는다. 이것은 EXPO의 핵심 철학이고, EXPO를 빠르게, 사용하기 좋게 만들어주는 부분이다.

## EXPO 앱과 Native 앱의 차이
![EXPO와 Native App 비교](https://lh3.googleusercontent.com/cYu8NWNwEl8EaW7nqJZ342bG0o36GSdCgEqCkE_pHhB4llyDnXgKy_Tf_Gtp8lSEXr2BCYELkSw)

먼저 오른쪽에 있는 네이티브 앱인 카카오톡을 볼까요?
카카오톡같은 네이티브 앱은 코드를 컴파일하고, 모바일 기기에 설치되어 OS 레이어와 직접 상호작용하며 네이티브 환경에서 동작합니다.

반면에 우리가 작성한 자바스크립트 코드는 EXPO 모바일 클라이언트 안에서만 동작하고, JavaScript 엔진으로만 동작하기 때문에 네이티브 언어 라이브러리를 소화해 낼 수 없습니다.
다만 EXPO 앱은 네이티브 앱이라서 OS 레이어와 상호작용을 대신 합니다. 그리고 코드를 작성할 때 컴포넌트화 된 모듈들을 이용할 수 있기 때문에 단순한 웹뷰 수준을 벗어나서 네이티브한 기능을 구현할 수 있습니다.







그 대신 EXPO는 자주 쓰이는 네이티브한 기능이나, 그런 기능을 이용하는 라이브러리를 내장하고 있고, React 컴포넌트로 쉽게 사용할 수 있게 준비해놓았습니다.

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTUwNjA3OTA2NSwxNjE0MDM1ODA4LC0xND
A3NzczNjY0LC0xNjgwODI1NjkxXX0=
-->