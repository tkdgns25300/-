먼저 자바스크립트 엔진은 메모리 할당이 일어나는 Memory Heap과 실행할 코드가 쌓이는 Call Stack으로 구성되어 있습니다.
그리고 Callback Queue라는 곳에서 비동기적으로 실행된 콜백함수를 보관하고 있는데 이벤트 루프는
Call Stack과 Callback Queue의 상태를 체크하여 Call Stack이 빈 상태가 되면, Callback Queue의 첫번째 콜백을
Call Stack에 추가하여 코드를 실행하는 방식을 말합니다.
Node.js는 이 Event Loop를 스레드로 사용하고 있기 때문에 싱글쓰레드 이지만, 비동기적인 코드도 CallStack Queue에
넣어놓았다가 추후에 처리 가능하므로 멀티쓰레드의 작동방식을 가진다고 볼 수 있습니다.