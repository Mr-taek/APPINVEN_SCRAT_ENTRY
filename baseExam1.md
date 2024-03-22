- Projects - > start new project -> name: ReadTalk(한글은 안됨)

- Steps
    1. Designer 모드 설정
    2. Palette에서 "button"과 "TextBox","TextToSpeech"를 스마트폰 화면에 드래그한다.
    3. visible 객체인 button,TextBox 는 화면에 나오나 Non visible 객체(사실상 기능)은 화면에 안나오고 스마트폰 바로 아래에 Non-visible components 란에 나온다.
    4. Blocks 모드로 설정한다.
    5. 왼쪽 여러 카테고리 중 Screen1 -> Button1 을 선택한다.
    6. 클릭했을 때의 기능을 만들기 위해서 when-do 기능중 when Button1 .Click 기능을 오른쪽으로 드래그 한다.
    7. 문자를 음성으로 바꿔야한다, 이번엔 카테고리에서 TextToSpeech1 컴포넌트를 선택한다
    8. 말하기 기능, 즉 행동하는 기능이 필요함으로 call 기능을 택해야한다. call TextToSpeech1 . Speak 를 드래그 해서 when-do 블록 사이에 넣는다
    9. 어떤 내용을 읽어야 하는지 필요하기에 TextBox1을 클릭하고 진한초록색박스(컴포넌트의 속성값)중에서 Text를 불러오는(TextBox1.Text)녀석을 드래그하여 call block 오른쪽에 붙여 넣는다
    10. 이제 휴대폰, 컴터에서 실행하면 성공적으로 작동이 된다.