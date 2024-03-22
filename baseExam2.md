- Projects - > start new project -> name: speakWhenphoneShaking(한글은 안됨)

- steps
    1. Designer 모드에서 아래의 컴포넌트를 드래그
        1. Sensors { AccelermeterSensor, }
        2. Media { TextToSpeech }
    2. Blocks 모드에서 아래 기능을 작성
        1. 스마트폰이 흔들렸을 때
            1. AccelermeterSensor1을 클릭하고 when - do .Shaking 기능을 드래그
        2. TextToSpeech1을 클릭하고 call TextToSpeech1.Speak 을 when-do 기능 안에 넣기
        3. message는 list로 만들고 첫번째 item은 "안녕하세요" 를 두번 item은 "안녕하세요"를 역으로 만드는 함수를 사용한 return 값을 집어 넣기.
    