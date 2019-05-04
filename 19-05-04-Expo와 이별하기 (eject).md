## EXPO의 동작 환경

![expo 동작 환경](https://lh3.googleusercontent.com/uI0fYPxqo0urSM60u_FbYdGwJmSspF5odKhn-RQAQufCtbJG5j9aFxuPqJ_6SXcFgCfBl2IfWVw)

어떤 구조로 동작하는걸까요?

EXPO는 로컬 개발환경에 두개의 서버를 띄웁니다.
EXPO 모바일 클라이언트에 react-native가 번들링 한 JavaScript 파일을 내려주기 위한 초록색 서버,
EXPO-CLI와 expo 모바일 클라이언트 둘 사이의 통신을 위한 서버(핑크색)을 하나 띄웁니다.


엑스포  모바일  클라이언트에

react-native가  번들링한  자바스크립트  파일을

내려주기  위한

초록색  서버

  

이렇게  두  서버를  띄워서  동작하는  환경입니다.

  

핵심은  엑스포  클라이언틉니다.

작성한  코드가  모바일  네이티브  환경에서  직접  구동되는게  아니고

엑스포  클라이언트  안에서

받아온  앱을

실행하는  방식입니다,

(넘겨)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0MzkyNDY0MDIsLTE0MDc3NzM2NjQsLT
E2ODA4MjU2OTFdfQ==
-->