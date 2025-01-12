## 1-2) 사전 과제

- (1) 동기와 비동기 프로그래밍에 대한 차이점을 설명해주세요.

 동기란 요청과 그 결과가 동시에 일어나서 시간이 얼마나 걸리던지 요청한 자리에서 결과가 주어져야만 다음 동작을 수행할수 있다. 비동기란 요청과 결과가 동시에 일어나지 않으며 하나의 요청에 그 응답이 즉시 처리 되지 않아도 그 대기 기간 동안 또 다른 요청에 대해 처리 가능한 방식이다.
 이 둘의 차이점은 동기는 설계가 직관적인 반면에 비동기는 여러 요청을 처리해야되기 때문에 동기식보다 설계가 복잡한 점이 있다. 어떤 작업을 하냐 목적의 차이라고 할수 있다.
 
- (2) 블로킹과 논블로킹의 차이점을 설명해주세요.

블로킹이란 브라우저가 실행되는 시간에 요청이 들어간다면 서버에서 설정한 응답 대기 시간이 약 2분이라면 2분동안 계속 대기 해야되는 상태를 말한다. 논블록이란 비동기 개념에서 만들어진 개념으로 브라우저가 대기하고 있는 시간에 다른 작업을 제약없이 할수 있는 상태를 말한다.

- (3) 본인이 주로 사용하는 언어에서 비동기 프로그래밍을 사용하는 방법을 설명해주세요.

 내가 사용하는 주 언어인 javascript는 싱글 스레드이긴 하지만 브라우저에서 사용하는 이벤트 루프로 인해서 멀티 쓰레드 처럼 작동한다. 또한 nodejs에서도 클라이언트의 방식을 차용해 요청을 서버내부에 메시지 형태로 전달하여 역시 이벤트 루프가 처리합니다.
 사용하는 방법은 크게 setTimeout,callback, promise, async await 등이 있다. settimeout은 호출이되면 실행할 함수와 시간을 인자로 받게 되는데 코드를 실행해보면 예상치못한 순서로 코드가 실행될수 있습니다. 응답이 오지 않았을때 실행할 함수가 실행되어버리면 undefined가 뜨기 때문에 주의해야됩니다. 콜백함수는 유명한 콜백지옥을 이르키는 함수로 방금 설명한 settimeout 함수와 사용한다면 예상된 결과를 얻을 수 있습니다. 콜백함수는 들여쓰기가 되기 때문에 가독성이 좋지 않습니다. 또한 promise 함수 역시 then 지옥에서 벗어 날수 없기 때문에 개인적으로는 잘 쓰지 않는 편입니다. 이를 메서드 체이닝 방식으로 하는데 중간에 오류가 나면 그 안에서 오류를 찾기가 쉽지 않기 때문입니다. 프로젝트가 복잡해짐짐에 따라 async/await 방식을 자주 사용합니다. 

- (4) 메세지 큐를 쓰는 이유에 대하여 2가지 예시를 서술해주세요. 

 먼저 큐란 데이터가 지나가는 관이라고 비유할수 있다. 분산되어 있던 요청처리를 한 곳(큐)에 두어 필요한 작업에 분산 시키는 방법을 하는 것이 그 목적이다. 큐에 넣어 놓기 때문에 나중에 처리 가능하고 실패한다고 다시 처리가능하고 서버의 성능을 개선 할 수 있다. 예시라면 비밀번호를 분실했을 때의 문자 인증 시스템이나 채팅서비스이다. 과연 이 서비스들이 메시지를 보내면 상대방에게 즉각 반영되는게 중요하지 않을 수 있다. 그 보다 앞서 실행 되었던 다른 이벤트의 처리가 더 중요 할수 있기 때문에 큐안에 앞서 있는 메세지를 먼저 처리한 후에 반영해도 늦지 않다는 말이 된다.
 
- (5) 본인이 작성한 서버 코드가 있는 github repo 주소를 제출해주세요. (CRUD 기능을 모두 포함하여야 하며, 서버에 대한 설명을 README에 작성해주시면 더욱 좋습니다.) 

https://github.com/godkor200/what-app => nestjs

https://github.com/godkor200/workoutScheduler => spring boot

- (6 - Optional) 해당 수업을 통해 꼭 배우고 싶은 주제 또는 지식이 있다면 자유롭게 서술해주세요. 
개인적으로 나에게 잘 맞는 백엔드 직무 찾기 (대용량 처리, 실시간 처리, 영상 처리, etc) 이 주제가 기대된다. 백엔드 개발을 시작하고 지금까지 백엔드 직무에서의 또 세분화는 생각해본적도 없었기 때문이고 백엔드 분야에서도 방향을 정하면 공부에 더 흥미를 갖고 몰입할수 있을꺼같아서 기대된다. 더불어 내가 업무에도 사용하는 aws를 더욱더 심도 있게 이해하는 기회가 됐으면 좋겠다.
