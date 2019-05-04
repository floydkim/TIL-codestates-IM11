# EXPO와 이별하기

## EXPO의 동작 환경

![expo 동작 환경](https://lh3.googleusercontent.com/uI0fYPxqo0urSM60u_FbYdGwJmSspF5odKhn-RQAQufCtbJG5j9aFxuPqJ_6SXcFgCfBl2IfWVw)

어떤 구조로 동작하는걸까요?

EXPO는 로컬 개발환경에 두개의 서버를 띄워 동작합니다.
EXPO 모바일 클라이언트에 react-native가 번들링 한 JavaScript 파일을 내려주기 위한 서버(초록색),
EXPO-CLI와 expo 모바일 클라이언트 둘 사이의 통신을 위한 서버(핑크색)을 하나 띄웁니다.

이 중 핵심은 엑스포 클라이언트입니다.
작성한 코드가 모바일 네이티브 환경에서 직접 구동되는것이 아니고, 받아온 앱을 엑스포 클라이언트 안에서 실행시킵니다.



<!--stackedit_data:
eyJoaXN0b3J5IjpbMTgwNzM3MjY4NiwtMTQwNzc3MzY2NCwtMT
Y4MDgyNTY5MV19
-->