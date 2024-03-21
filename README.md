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
        7. 

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
            1. when-do : 갈색, if문 같은 거임. 
            2. call~.행동 : 보라색, 행동을 하도록 요청(호출). 이것만 when-do가 없으면 그냥 시작하자마자 기능 작동화 되는거임. 초기화 할때 써도 될 듯함.
            3. set Component.ComponentPropertires to ComponentPropertiresValue : 진한 초록색 구성요소의 properties를 ComponentPropertiresValue 값으로 변경(설정)하는 기능.
            4. block 오른쪽에 홈이 있는 곳 : 주황색/초록색 명령 블록은 오른쪽에 홈이 파여져 있다. 끼워질 블록은 수행할 명령의 상세한 값이다.
            5. get.properties : component의 속성값을 가져오는 기능.



- Component 의 고찰 : 
    - 컴포넌트란 ? : 가속도센서 , 스피커 사용 , 타이머 , GPS 등 앱을 구성하는 구성요소들을 의미한다.
        - 컴포넌트의 기본 속성(초기값)은 Designer->components에서 구성요소를 선택하고 -> 바로 오른쪽 properties 탭에서 상세한 초기 속성을 구성할 수있다.
        - 컴포넌트의 기본 속성은 block에서도 변경할 수있다.
    - Components 종류
        - User Interface
            1. TextBox : 숫자나 글을 입력받고 싶을 때 사용하는 component.
                - 
        - Drawing and Animation
            1. Canvas : 