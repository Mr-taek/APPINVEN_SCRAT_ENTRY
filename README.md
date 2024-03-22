# 앱 인벤터를 사용한 강의를 위한 자료 입니다. 개념과 사용법과 핵심예제이 작성되어 있습니다

#### 참고서적

1. (꿀잼) 앱 인벤터 - 쉽고 재미있는 앱 프로그래밍 세계
2. 앱인벤터 한권으로 끝내기 - 첫걸음부터 나만의 앱 제작까지



- 서두
    ```
    앱 인벤터는 어려운 코딩과정 없이 블록을 쌓으면서 놀이처럼 앱을 만들 수 있습니다. 스마트폰에서도 실시간으로 테스트 해보면서 앱을 구동할 수 있죠

    앱 인벤터를 통해 앱 개발이 어렵다는 고정관념(?).... 을 날려 버리고 여러분의 재능을 마음껏 발산할 수 있도록 안내하겠습니다. (앱 개발이 쉬운건 아니지 ㅋ...)

    스마트폰 앱 제작을 위해선 자바같은 것들을 공부해야 하는 번거로움이 있다, 그 와중에 앱 인벤터는 이 번거로움을 해결할 수 있다.
    ```
    - 앱 인벤터란 ? : 안드로이드 기반 휴대폰이나 에뮬레이터에 앱을 개발할 수 있도록 해주는 프로그램이다. 앱 인벤터는 구글에서 만든 chrome 브라우저에서 진행되기 때몬에 크롬을 다운받고 안드로이드 기반 스마트폰을 준비하는 것이 필요하다. 또 자체 서버가 있어서 그곳에서 바로 작업을 저장할 수 있고(clouding computer) 프로젝트를 쉽게 진행할 수 있다.
    - 앱 인벤터로 어떤 기능을 ? : 안드로이드 휴대폰의 "기능" 대부분을 사용할 수 있께 설계되었다. 프로그램을 통해 정보저장/실행반복/조건문을 사용이 된다. 
        1. gps센서에 접근도 가능해 현재 위치를 알려주는 앱을 만들 수도 있다. 
        2. 자동차를 어디에 주차해 뒀는지 기억하는 앱
        3. 콘서트에 같이 간 친구를 찾는 앱
        4. 박물관이나 혼잡한 대형 쇼핑물에서 활용할 수 있는 개인용 길찾기 앱도 만들 수 있다.
        5. 사랑하는 사람에게 "뽀고싶다" 라는 문자를 주기적으로 보내게 하거나
        6. 운전 중에 켜 두고 문자나 연락이 왔을 때 "운전 중입니다" 라는 문자 메시지를 보내주는 앱도 만들 수 있다.
        7. 문자를 직접 음성으로 읽어주는 앱도 만들 수도 있다.
        8. 앱 인벤터는 인터넷과 연결하여 사용할 수 있어 웹 페북이나 트위터 같은 sns와 연동하여 소통하는 앱을 만들 수도 있다.
    - 필요 작업환경
        1. windows , Android기반 기기 , Mac OS, GNU/Linux 에서 사용가능하다.

[앱 인벤터 준비, Hello world 예제와 소스코드 공유부터 앱다운까지](#앱-인벤터-준비)

[앱인벤터 기능별 사용법](#앱-인벤터-기능사용법)

### 앱 인벤터 준비

1. Google chrome을 다운로드 한다.
2. https://appinventor.mit.edu/ 에 접속하여 create Apps 를 클릭한다

3. 앱 인벤터 테스트 환경 준비하기
    1. 같은 WIFI 환경 : 같은 WIFI 네크워크(같은공유기의 WIFI)를 사용하면 앱과 앱 인벤터가 "실시간"으로 동기화한다.
        1. 안드로이드 휴대폰에서 "MIT A2 Companion" 을 설치한다.
        2. 연결 방법은 Hello world 예제의 마지막에 있다.
    2. Emulator 사용하기 : 여러 사람들에게 보여주는 수업에서 스마트폰으로 굳이 안 보여줄 경우이다
        1. https://appinventor.mit.edu/explore/ai2/setup-emulator 에 진입한다. (만약 잘못된 곳이라면 첫 홈페이지에서 emulator을 검색해서 installing을 찾자.)
            - window 버전 설치법 : https://appinventor.mit.edu/explore/ai2/windows
        2. Download the installer 로 적힌 파란색을 잘 찾아서 다운로드한다. (다운로드 시간이 좀 걸린다.)
        3. 다운로드 .exe 을 실행하면 꼭 경로는 "C:\Program Files\MIT App Inventor" 로 되어 있어야 한다.
        4. 설치가 다 되면 바탕 화면(command창에 aiStarter) aiStarter를 실행한다.
        5. cmd 창의 마지막에 "Hit Ctrl-C to quit" 가 나오면 성공이다.
        6. cmd 창을 켜둔 상태에서 app invertor 브라우저에서 연결(Connect) -> Emulator(애뮬레이터) 를 클릭하면 자동으로 aiStarter을 찾아서 실행한다.
        7. aiStarter에서 화면이 켜진 순간 브라우저 화면의 스마트폰 기능이 바로 나와야 한다. 만약 안나온다면 다시 재접속시켜야한다.
        - 단점: 이게 소리가 안나와서 시각적인 부분만 가능하다. 

3. Hello World 예제
    1. Projects - > start new project -> Project name의 첫글자는 꼭 영문자이며 뒤부터 숫자와 밑줄이 올 수 있다. -> 확인을 누르면 자동으로 앱이 등장한다.
    2. 왼쪽 Palette 에서 Sensors 섹터를 클릭한다. 휴대폰에 있는 센서들을 의미하는 것같다.
    3. AccelerometerSensor 을 드래그 하여 화면 휴대폰 사진 중앙 하얀색에 올려놓는다. 가속도 센서가 움직임을 인식하게 된다.
    4. Media Sector에서 TextSpeech를 올려 놓는다.
    5. 두 개의 component가 화면 오른쪽에 Components 란에 등록 되어 있다. 기본 값으로 "All components"로 되어 있는데 앞에 두개 기능은 Non-visible Component이다.
    6. 화면 오른쪽 내 이메일이 있는 곳 아래에 "Designer" "Blocks"가 있는데 현재 "Designer" 모드가 되어 있다. "Blocks"를 클릭한다.
        - 앱 인벤터의 독특한 기능이 바로 "Block"이기도 하다. 수행하는 작업들을 블록으로 쌓아서 실행한다.
    7. 이제 화면 오른쪽에 보면 "Palette"가 아니라 "Block" 카테고리가 생기고 그 아래 다양한 Components가 생긴다. components를 클릭하면 블록을 쌓는 카테고리 화면 왼쪽에 어떤 직사각형이 나열된 box가 생성되는데 그 중에서 2번째 when {AccelerometerSensor1}.Shaking 을 클릭하여 오른쪽 하얀색 빈칸에 옮긴다.
    8. 이번엔 TextToSpeech1 Components를 클릭해서 Call {TextToSpeech1}.Speak 를 선택해서 가속도센서 블록 사이에 집어 넣는다.
    9. built-in(공통 블록)에서 Text block을 선택하고 TextToSpeech의 오른쪽에다가 해당 블록을 끼워 넣는다.
    10. Textbox 흰색 공간을 클릭하여 "HELLO WORLD"를 적어놓고 Enter을 누르면 완성이다.
    11. 화면 윗 Bar에서 Connect(연결) AI COMPANION(AI 컴패니언)을 클릭해서 휴대폰에 MOT APP INVENTOR을 실행하여 QR로 연결시킨다.
    12. 이제 휴대폰을 흔들면 "HELLO WORLD"라는 소리를 휴대폰이 내뿜는다.
    13. HELLO WORLD 예제 끝

4. 앱을 휴대폰에 저장하기
    ```
    스마트폰에 다운로드한 앱의 확장자는 대개 .apk 이다. 앱 인벤터에서 만든 앱을 저장하고 싶다면 .apk로 변환하면 된다.
    주의할 점이 있다
        1. QR 코드를 다른 사람들에게 보내면 앱이 다운되지 않는다.
        2. 앱이 켜져있고 그 자리에서 QR코드를 인식해야 다운로드가 된다.
        3. 공유가 필요하면 .apk를 내 폰에 다운받고 공유하면 된다.
        4. 이제 이 .apk는 구글 플레이 스토어에 올리기도 가능해진다.
    ```
    1. 테스트를 끝냈다면 브라우저에서 build(빌드) 를 클릭한다
    2. Android App(.apk)를 클릭한다.
    3. 기다리다보면 qr코드가 나온다. 해당 코드를 MIT AI2에서 스캔한다
    4. 휴대폰에서 링크를 타고 자료를 다운받는다. 해당 자료를 내 폰에서 설치한다
    5. 그러면 내 휴대폰에 해당 기능이 담긴 앱이 사용이 가능해진다.

5. 제작한 app을 다른 사람이 활용시키기 : app inventor 브라우저에서 Project - > Import Project(선택된 프로젝트 (.aia)를 내 컴퓨터로 내보내기) 를 클릭 -> 해당 파일을 사람들에게 뿌리고 Project에서 내 컴퓨터로 프로젝트(.aia)가져오기 한다.



### 앱 인벤터 기능사용법

- Designer, Block : 앱 인벤터의 처음 기능은 크게 2가지로 나뉘어져 있음
    - 위치 : 브라우저의 오른쪽 이메일 아래에 위치한다.

    - Designer : 스마트폰에 사용할 기능과 화면 배치를 디자인
        1. 팔레트 (Palette)
        2. Components : 현재 앱에 사용된 스마트폰의 기능.
            - 세부 구성
                - All Components : 모든 구성요소를 보이게 한다
                - visible : 실제 화면에 보이는 front-end 기능
                - Non-visible : back-end 기능
        3. Properties : 특정 components를 선택하면 해당 구성요소가 가질 수 있는 특성이 있는데 이 특성을 조절한다. 예를들어 가속도센서는 얼만큼 민감하게 반응할 것인지를 조절할 수 있습니다.
        4. Viewer : 화면 중앙 스마트폰 그림이 있는 곳. 실제 앱이 휴대폰에서 어떻게 보이는지 확인할 수 있음.
    - Blocks : 사용하기로 한 기능의 구성/추가/삭제 하는 곳
        ```
        Block이 사실상 가장 app inventor에서 가장어렵고도 기능을 만들 수 있는 핵심 장소이다.
        
        기능을 알기 전에 when , do , call , shaking이 정확히 어떤 의미인지 파악하고 블록을 쌓으면 블록을 쌓고 프로그래밍이 어떻게 이루어지는지 이해하는 데 충분하고도 핵심적인 이해가 이루어질 것이다.
        ```
        - Block 카테고리 구성
            1. Built-in-Drawers(Built-in) : 자주 쓰이는 명령블록들을 모아 놓은 공간.
            2. Any component(컴포넌트 Drawers) : Designer에서 사용하도록 drag한 구성요소가 있는 곳.
            3. Block viewer : 화면 중앙 흰색바탕의 블록을 옮겨서 프로그램을 제작(기능구성)하는 화면 공간.
        - Block 실행순서
            1. 가로로 연결되는 블록들은 한번에 실행된다.
            2. 세로로 연결되는 블록은 위에서 아래로 명령을 실행한다. Block Stack 이라고 한다.
        - Block 기능 단어 해석
            1. when-do : 갈색, if문 같은 거임. 중요한 내용
                - 특징
                    1. 황색 block은 지역변수를 선언할 수 있는 특징이 있음. 여기서는 지역변수를 생성이 가능함. 즉 황색 block이 끝나면 지역변수도 소멸하게 됨.
            2. call~.행동 : 보라색, 행동을 하도록 요청(호출). 이것만 when-do가 없으면 그냥 시작하자마자 기능 작동화 되는거임. 초기화 할때 써도 될 듯함.
            3. set Component.ComponentPropertires to ComponentPropertiresValue : 진한 초록색 구성요소의 properties를 ComponentPropertiresValue 값으로 변경(설정)하는 기능.
            4. block 오른쪽에 홈이 있는 곳 : 주황색/초록색 명령 블록은 오른쪽에 홈이 파여져 있다. 끼워질 블록은 수행할 명령의 속성 값이거나 명령어 이다.
            5. get.properties : component의 속성값을 가져오는 기능.
            6. 왼쪽 이 튀어나오고 어떤 동사도 없는 block : 해당 컴포넌트(block)의 속성값들이다. 기능을 수행할 때 해당 컴포넌트의 속성값을 변경해야할 때 사용한다.



- Component 의 고찰
    - 컴포넌트란 ? : 가속도센서 , 스피커 사용 , 타이머 , GPS 등 앱을 구성하는 구성요소들을 의미한다.
        - 컴포넌트의 기본 속성(초기값)은 Designer->components에서 구성요소를 선택하고 -> 바로 오른쪽 properties 탭에서 상세한 초기 속성을 구성할 수있다.
        - 컴포넌트의 기본 속성은 block에서도 변경할 수있다.
    - 컴포넌트 이름 바꾸는 법(block에서 구분히 편해짐) : Design 모드에서 All Components 구역에 보면 하단에 "이름 바꾸기" 가 있음. 바꾸고자 하는 컴포넌트를 선택해서 이름바꾸기 하면 끝.
    - Components 종류
        - Screen : 스크린이 처음에 기본적으로 나오지만 Screen도 components의 하나임
            - Add Screen(스크린 추가...) : 스크린을 추가하는 버튼. 화면 중앙에서 위쪽에 보면 버튼이 있음.
            - Funcs
                1. 언제{}.초기화되었을때 : 
        - Built-in (내장 함수, 내장 컴포넌트)
            - 제어 : if/for 문이 있음.  screen제어문이 있음
                - if문 종류
                    - 용어해석
                        1. 아니고 만약 = else if
                        2. 아니라면 = else
                    1. 만약 {boolean} 이라면 실행 {실행 block}: boolean 자리엔 "논리" block이 옴. 실행 block엔 call(호출), set(지정하기) 등으로서 실행을 하는 녀석이 올 수있음.
                    2. 만약 {} 이라면 실행 {} 아니라면 {} : if (bool) {} else {} 랑 같은 개념
                    3. 톱니바퀴로 조절해서 쓰면 됨.
                - for문 종류
                    1. 각각 반복 {variable} 시작 {startNum} 끝 {endNum} 증가 {increment} : for (variable=startNum;startNumendNum;variabble+=increment) 랑 같은 개념
                    2. 조건 반복 조건 {bool} 실행 {실행문} : while 문이랑 같음. bool이 True 이면 계속 반복임.
                2. open another screen screenName {} (다른 스크린열기 스크린이름 {}) : 스크린 추가를 했을 때 원하는 스크린으로 이동하는 기능을 한다.

            - 논리 : bool 기능이 담겨져 있음. =>< 등이 있는 거임.
            - 변수 : 변수를 만드는 것임
                1. 전역변수 만들기 {이름} 초기값 {value} : 말 그대로 전역변수 "이름" 을 만들고 value 를 초기값으로 하는 전역변수를 만드는 거임. 
                2. 지정하기 {전역변수} 값 {value}: 전역변수의 값을 value로 할당하는 선언문임.
            - Text : Text와 관련된 모든 함수(block)이 존재한다.
                - Funcs
                    1. " " : 빈칸 안에 글을 적어 넣는 곳
                    2. join : 위에서 아래로 string을 추가한다. string+"_"+string 에서 +와 같은 기능이다. 톱니바퀴를 클릭해서 join시킬 string의 개수를 조절할 수 있다.
                    3. contain text {"문자열"} piece {"문자"} : true/false , 문자열안에 문자가 있는 지를 확인.
            - Lists : list 자료 구조와 관련된 모든 것이 있다.
                - 핵심사항
                    1. list의 인덱스는 1부터 시작이다.
                - Funcs
                    1. make a list : list를 만든다. 톱니바퀴를 통해 포함시킬 item의 개수를 조절할 수 있다.
                    2. 위치 구하기 항목 {index} 리스트 {리스트 변수}(select list item list {리스트변수} index {index}) : 리스트 변수의 인덱스에 있는 값을 return한다. 인덱스는 1부터 시작함을 명심해야한다.
                    3. replace list item list {list변수} index {index} replacement {대체할 값} : list변수에 있는 index 자리에 "대체할 값"으로 값을 변경한다.
        - Sensors : 이름 그대로 센서임. Non-visible 한 Components가 있음
            - 가속도센서(Accelermeter) : 가속도에 대한 센서임
                - Funcs
        - User Interface
            1. TextBox : 숫자나 글을 입력받고 싶을 때 사용하는 component.
                - 
            2. Button : 버튼이다.
                - properties
                    1. image : 버튼에다가 이미지를 불러와서 꾸밀 수 있다. 이미지는 꼭 염문이어야 하며 특수문자가 없어야 한다.
                    2. Text : 버튼이 어떤 버튼인지를 적을 수 있다.
            3. 목록선택버튼 : 버튼을 누르면 메뉴bar처럼 옵션을 선택할 수 있게 함.
                - 주의사항
                    1. 목록선택은 사전에 Designer 모드에서 "요소문자열" properties 에서 콤마로 옵션을 미리 생성할 수 있다.
                    1. 동적으로 추가하려면 Bolck 모드에서 when{}.선택전에 set{}.element 값 {value}에서 value에다가 list를 집어 넣으면 된다. list를 넣는 이유가 애초에 "요소문자열"이 list를 받기 때문이다(Set the list of choices from a string of comma-separated values.)
                - Funcs
            4. 목록뷰
        - Media : 사진이나 음성 관련 기능 컴포넌트가 있음
            - 음성인식 , baseExam3.md를 참고하면 이해가 더 빨라짐.
                - Funcs
                    1. 언제 {}.텍스트가져온 후에 실행 {} : 호출{}.텍스트가져오기 를 뜻한다. 이 녀석을 실행하면 자동으로 구글 음성인식이 실행되고 구글이 지가 알아서 말 끝난 것같으면 종료키고 텍스트 가져오기가 끝난다. 이때 끝났을 때부터 텍스트가져온 후 이다.
                    2. 호출{}.텍스트가져오기 : 녹음 시작이라는 뜻임
                    3. 호출{}.정지 : 녹음 종료란 뜻임.
                    4. {}.결과 : 음성인식 해서 text로 변환한 결과 문자열 이란 뜻. 문자열을 반환함.
            - Player(플레이어) : 노래를 재생시킨다.
                - Funcs
                    1. {}.재생중여부 : bool, 현재 Player가 재생중인지 아닌지를 알려준다.
            - Camera : 카메라, 안드로이드 폰에 내장된 카메라 기능을 가져와서 사진을 찍습니다
                - Funcs
                    1. call{}.사진찍기 : 내장된폰의 사진 기능을 가져옵니다
                    2. when{}.AfterPicture : 사진 기능이 완료 된후의 기능입니다.
            - Sound(소리) : 아주 짧게 소리/진동을 내는 기능. 소리내는 기능은 Player와 같으나 Sound는 아주 짧게 내보냄. 나오는 소리 간격은 properties로도 조절이 불가능함.
                - Funcs
                    1. call{}.Vibrate(진동하기) 밀리초 {숫자} : 숫자 밀리시간만큼 진동을 일으킨다.
        - Social(소셜) : 전화걸기,이메일
            - PhoneCall(전화)
                - Funcs
                    1. set{}.전화번호 값 {전화번호 Text} : PhoneCall 컴포넌트당 하나의 전화번호를 지정할 수 있음. 전화번호 Text 의 전화번호를 전화번호변수에 할당하는것임.
                        - 
                    2. call{}.MakePhoneCall(전화걸기) : 전화변수에 있는 값으로 전화를건다. 단, 바로 전화가 걸리지 않고 폰에 있는 전화기능을 가져온 다음 거기다가 변수 값을 집어 넣는다. 전화는 내가 직접 통화하기를 따로 눌러야 한다.
                    3. call{}.DirectMakePhoneCall(다이렉트전화걸기) : 2번이 아닌 자동으로 전화걸기인데, 이게 구글에서 관리하기 때문에 이 기능은 사실상 사용이 불가능한 상태라고함.
                        - 불가능 참고 사이트 : https://groups.google.com/g/mitappinventortest/c/z2smpTougx4?pli=1
        - Drawing and Animation
            1. Canvas : 그림을 그리는 기능을 한다.
                - properties
                    1. BackgroundColor : 그림판의 배경색
                    2. BackgroundImage : 그림판의 배경 이미지
                    3. FontSize : The font size of text drawn on the canvas.
                - Funcs : 보면 그냥 대부분 슥 보면 어떤 의미인지 알 수 있는 것들이다.
                    1. when{}.Dragged : 손으로 드래그 했을 때
                    2. when{}.Flung : Flung은 내던지다, 팽개치다란 뜻. 즉 손끝으로 휙 했을 때를 의미하는 듯.
                        - 지역변수
                            1. X ,Y : 터치한 지점의 좌표
                            2. 속도 : ROOT(V_X^2+V_Y^2) 의 값
                            3. 방향 : 각도 값. 원의 오른쪽 값이 0도, 반시계 방향으로 +이고 최대 180도이다. 시계방향은 -값으로서 여기도 -180임. 즉 각도는 180~-180 사이의 값을 갖음.
                            4. V_X,V_Y : X,Y 각각 축의 속도를 의미함.
            2. ball/imageSprite : 둘다 기능은 같다. imageSprite는 외부이미지를 덧붙일 수 있다는 특징이 있다
                - Funcs
                    1. 호출{}.좌표바라보기 x{} y{} : x,y위치로 이미지의 heading 변경함.
                    2. 호출{}.스프라이트바라보기 : ball/imageSprite를 대상으로 Sprite가 바라보는 방향을 변경함. 항상 대상이 되는 타겟과 직선이되도록 각도를 유지하면서 움직임.
        - Storage(저장소) : 데이터 저장을 위한 Components가 있음
            - 참고 예제
                1. baseExam7.md
            - TinyDB
                - 용어
                    1. tag(태그) : key의 개념. key:value 방식으로 값을 저장하기 때문에 db에서 값을 찾을땐 tag로 찾게 됨.
                - Funcs
                    1. call{}.태그가져오기 : 현재 DB에 있는 모든 tag를 list형태로 반환함.
                        - skill
                            1. list에서 길이구하기 리스트 의 오른쪽에 붙이면 현재 db에 있는 모든 태그의 개수를 구할 수있음.
                    2. call{}.값가져오기 : 호출block 주제에 값만 가져와서 사용에 조금 애를 먹었었음. 암튼 태그값을 주면 그 태그의 value를 return함.