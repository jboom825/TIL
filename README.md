2021/04/14
- 마크다운 문서를 작성하기 위해 마크다운 문법도 익혀야 한다니.. 일단 써놓고 나중에 좀 바꾸자
- JUnit 정리중. 거의 번역만 해서 올리는중
- @TestInstance 어노테이션 : JUnit 테스트의 생명주기를 결정함.
- Lifecycle.PER_CLASS 와 Lifecycle.PER_METHOD(기본값)가 있다.
- PER_CLASS로 하면 클래스단위로 인스턴스를 생성하고 JUnit Test Class의 모든 함수들이 동일 자원을 공유한다.
- 즉, 메서드1의 결과가 메서드2에 영향을 줄 수있다.(맴버변수값 변경)
- 테스트 결과를 의도적으로 전부 혹은 일부 공유해야 하거나 자원소비가 많은 작업(DB접속, 대용량파일IO)시 고려해봄직함.
- BeforeEach 나 AfterEach 가 원래는 static 해야하지만 PER_CLASS 일경우 static으로 할 필요 없으며 중첩된 테스트(@Nested)에서도 사용가능하다.(원래안됨)
