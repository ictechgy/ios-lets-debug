아래의 문제를 해결하기 위해서 참고할 자료는 [WWDC 세션](https://developer.apple.com/videos/play/wwdc2018/415)에서만 찾습니다.    
그 외에는 [LLDB 공식 문서](https://lldb.llvm.org/)까지만 허용합니다.  
다른 곳에서 자료를 찾는 것은 반칙입니다. 여러분의 양심에 맡깁니다.

### 참고할 WWDC 세션 힌트

* Debugging Tips and Tricks
* Debugging with Xcode 9
* Visual Debugging with Xcode
* LLDB: Beyond "po"

&nbsp;

### 문제

- **ViewController.swift 파일의 23번째 줄에 브레이크 포인트를 설정하려면 입력해야 하는 LLDB 명령어는?** 
  breakpoint set --file ViewController.swift --line 23
  br s -f ViewController.swift -l 23
  b ViewController.swift:23

&nbsp;

- **`changeTextColor`라는 심볼(함수나 변수?)에 브레이크 포인트를 설정하기 위해 입력해야 하는 LLDB 명령어는?** 
  breakpoint set --name changeTextColor
  b changeTextColor
  `lldb also supports command completion for source file names, symbol names, file names, etc.`

&nbsp;

- **Breakpoint Navigator를 통해 `titleLabel`의 `text`가 `"두 번째 뷰 컨트롤러!"`인 경우에만 작동을 일시정지하고 `titleLabel`의 `text`를 출력하는 액션을 실행하도록 설정해보세요**
  ![image](https://user-images.githubusercontent.com/39452092/125762551-4ea2f992-51d4-44a2-b5aa-285d37c105a8.png)
  위에 이미지처럼 조건 설정하고, 필요없는 @objc 메서드는 disable 해주세요
  ![image](https://user-images.githubusercontent.com/39452092/125762586-eefa02dc-af2a-427d-9a26-7fd6f5d47b10.png)
  -> 나는 Symbol에 viewDidLoad를 썼는데, 이렇게 해도 잘 된다. 
  

&nbsp;

- **오류(Error) 혹은 익셉션(Exception)이 발생한 경우 프로세스의 동작을 멈추도록 하는 방법에 대해 알아봅시다**
  Breakpoint Navigator에서 아래쪽의 + 기호를 눌러 Error나 Exception에 대한 breakpoint를 추가한다. 

  

&nbsp;

- **View Controller의 뷰 위에는 사용자 눈에 보이지 않는 뷰가 있습니다. 이 뷰의 오토레이아웃 제약을 확인해서 알려주세요**

  

&nbsp;

- **디버그 모드로 실행중인 상태에서 사용자 눈에 보이지 않는 뷰의 색상을 분홍색으로 변겅해보세요**

  

&nbsp;


- **두 번째 뷰 컨트롤러의 뷰가 화면에 표시된 상태에서, 두 번째 뷰 컨트롤러 까지의 메모리 그래프를 캡쳐해보세요**

  

&nbsp;


- **LLDB의 특정 명령어의 별칭을 설정해줄 수 있는 명령어는 무엇일까요?**
  command alias 별칭명 "원래 명령어명"

&nbsp;


- **LLDB의 `v`, `po`, `p` 명령어의 차이에 대해 알아봅시다**
  v:
  po:
  p: 

&nbsp;

WWDC 45:48 Symbol에 대한 설명 - https://developer.apple.com/videos/play/wwdc2018/415/?time=200
https://lldb.llvm.org/index.html
