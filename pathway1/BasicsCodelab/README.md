> [코드랩 - Jetpack Compose basics](https://developer.android.com/codelabs/jetpack-compose-basics?continue=https%3A%2F%2Fdeveloper.android.com%2Fcourses%2Fpathways%2Fjetpack-compose-for-android-developers-1%23codelab-https%3A%2F%2Fdeveloper.android.com%2Fcodelabs%2Fjetpack-compose-basics#3)

#### 0. 코드랩 소개
- 컴포즈를 맛보기 위해 `컴포저블 함수 만들기`, `컴포저블 함수 내에서 state 관리하기`, `리스트 만들기`, `애니메이션 구현하기`, `스타일과 테마 추가하기` 등을 배워봅시다. 리스트가 있고, 리스트의 각 아이템에 펼쳐지는 애니메이션이 적용된 화면을 구현해 봅시다.  
- <img width = "200" src="https://developer.android.com/static/codelabs/jetpack-compose-basics/img/8d24a786bfe1a8f2.gif" />

#### 1. 컴포즈 시작하기
- `@Composable` 어노테이션을 붙여서 컴포저블 함수를 만듭니다.
- XML 파일 대신, 액티비티의 onCreate() 내에서 `setContent` 를 선언하고 이 내부에서 컴포저블 함수를 호출하면 됩니다.
- UI를 앱 빌드 없이 안드로이드 스튜디오 내에서 미리 보고 싶다면 `@Preview` 어노테이션을 컴포저블 함수에 붙여주면 됩니다.

#### 2. Surface 사용하기
- `Surface` 로 배경 영역을 지정할 수 있습니다. 배경의 색상도 설정할 수 있습니다. `Surface` 는 머티리얼 디자인이 적용됩니다.

#### 3. Modifier 사용하기
- `Surface` 또는 `Text` 같이, 기본적으로 제공되는 컴포즈 UI 요소들은 대부분 modifier 라는 파라미터를 갖고 있습니다. 이 파라미터로 Modifier 인스턴스를 생성하여 전달하면 됩니다.
- Modifier 인스턴스는 해당 UI 요소가 부모 UI 요소 내에서 어디에 위치해야 하는지, 어떻게 보여야 하는지 등을 결정합니다.
- 예시로 Text 에 padding 을 적용해봅시다.
  ~~~kotlin
  Text(text = "Hello $name!", modifier = Modifier.padding(24.dp))
  ~~~

#### 4. 컴포저블 함수 재사용하기
- 비슷한 UI를 구현하기 위해 서로 다른 여러 개의 컴포저블 함수는 만들 필요는 없습니다. 한 개의 컴포저블 함수를 만들어두고, 재사용하면 됩니다.
- 컴포저블 함수 재사용을 위한 가장 좋은 방법은 Modifier 를 컴포저블 함수의 파라미터로 받는 방법입니다(디폴트 값은 Modifier로 설정). 컴포저블 함수를 호출하는 부분에서 Modifier를 자유롭게 바꿀 수 있으므로, 완전히 똑같은 UI 뿐만 아니라 비슷한 UI도 하나의 컴포저블 함수만 가지고 구현할 수 있습니다.
- 예시로 Title 라는 컴포저블 함수를 만들어 봅시다. Title 컴포저블은 여러 곳에 재사용될 수 있습니다.
  ~~~kotlin
  // 호출부
  Title(modifier = Modifier.aaa)
  Title(modifier = Modifier.bbb)
  
  // 컴포저블 함수
  @Composable
  fun Title(modifier: Modifier = Modifier) {
      Surface(
          modifier = modifier,
          color = MaterialTheme.colorScheme.primary,
      ) {
          Greeting(name = "Android")
      }
  }
  ~~~
  
#### 5. Column(열)과 Row(행) 만들기
- 이어서..
