> [코드랩 - Jetpack Compose basics](mpose-basics?continue=https%3A%2F%2Fdeveloper.android.com%2Fcourses%2Fpathways%2Fjetpack-compose-for-android-developers-1%23codelab-https%3A%2F%2Fdeveloper.android.com%2Fcodelabs%2Fjetpack-compose-basics#0)

#### 코드랩 소개
- 컴포즈를 맛보기 위해 `컴포저블 함수 만들기`, `컴포저블 함수 내에서 state 관리하기`, `리스트 만들기`, `애니메이션 구현하기`, `스타일과 테마 추가하기` 등을 배워봅시다. 리스트가 있고, 리스트의 각 아이템에 펼쳐지는 애니메이션이 적용된 화면을 구현해 봅시다.  
- <img width = "200" src="https://developer.android.com/static/codelabs/jetpack-compose-basics/img/8d24a786bfe1a8f2.gif" />

#### 컴포즈 시작하기
- `@Composable` 어노테이션을 붙여서 컴포저블 함수를 만듭니다.
- XML 파일 대신, 액티비티의 onCreate() 내에서 `setContent` 를 선언하고 이 내부에서 컴포저블 함수를 호출하면 됩니다.
- UI를 앱 빌드 없이 안드로이드 스튜디오 내에서 미리 보고 싶다면 `@Preview` 어노테이션을 컴포저블 함수에 붙여주면 됩니다.

#### Surface 사용하기
- `Surface` 로 배경 영역을 지정할 수 있습니다. 배경의 색상도 설정할 수 있습니다. `Surface` 는 머티리얼 디자인이 적용됩니다.

#### Modifier 사용하기
- 이어서...
