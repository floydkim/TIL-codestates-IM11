React Native로 모바일 앱 개발

공식 문서의 안내에 따라 expo로 boilerplate를 만들게 되었다.
```bash
$ expo init
```
명령을 실행하면 navigation이 없는 빈 스크린 / navigation을 포함한 boilerplate를 선택할 수 있고, 프로젝트에서는 앱의 다양한 기능을 구분짓기 위해 navigation이 필요했다.

이 글에서는 React Navigation을 이용해 화면 전환 구현을 어떻게 하는지, 인증과 자동 로그인 구현을 어떻게 했는지 돌아본다.

---

기본적으로 3개의 스크린과 이 스크린을 이동하기 위한 하단 탭 네비게이터를 제공한다.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA2OTYyMDcxNV19
-->