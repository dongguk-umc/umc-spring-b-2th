# Server 6주차 워크북

# 핵심 키워드 🎯

- API
- Http 패킷
- Http 메소드
    
    ![Untitled](Server%206%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20%E1%84%8B%E1%85%AF%E1%84%8F%E1%85%B3%E1%84%87%E1%85%AE%E1%86%A8%200a7a448daafb417a9ee28341fba6b51e/Untitled.png)
    
    - GET
    - POST
- 데이터 포맷
    
    [https://blog.jgtradeplus.com/3데이터포맷-xml과-json/](https://blog.jgtradeplus.com/3%EB%8D%B0%EC%9D%B4%ED%84%B0%ED%8F%AC%EB%A7%B7-xml%EA%B3%BC-json/)
    
    [https://velog.io/@53_eddy_jo/RESTful한-세계에서의-POST와-PUT의-차이-거기에-FETCH까지](https://velog.io/@53_eddy_jo/RESTful%ED%95%9C-%EC%84%B8%EA%B3%84%EC%97%90%EC%84%9C%EC%9D%98-POST%EC%99%80-PUT%EC%9D%98-%EC%B0%A8%EC%9D%B4-%EA%B1%B0%EA%B8%B0%EC%97%90-FETCH%EA%B9%8C%EC%A7%80)
    
- API Sheet
- path variable

# 6주차 수업 후기 📢

- 6주차 **수업을 듣고 서로 느낀 점을 이야기해주세요!**
- **핵심 키워드에 대해 완벽하게 이해했는지? 혹시 이해가 안 되는 부분은 뭐였는지?
서로 이야기해주세요!**

### 📝 실습 체크리스트

- [ ]  실습 1. 인스타그램 기능 List up

# !주의사항

1. **과제 피드백 기반 진행입니다** - 한명씩 본인의 **과제를 발표**하는 시간 그리고 해온 **과제에 대한 피드백**을 하는 시간 (ex:전 이렇게 생각해서 이런 부분 다르게 해왔는데 저것도 괜찮은 것 같아요!)이 **무조건 기반**이 되어야 합니다!
2. 부가적으로 **워크북에서 제공되는 키워드 혹은 강의에서 들은 디테일 적인 부분**에서 더 토의해봐도 좋을 것 같습니다

# 논의해보면 좋은 것들 🔥

- 프레임워크란 무엇인가?
    - 라이브러리는 무엇인가?
- restful api 가이드 찾아보기
    
    # REST API 디자인 가이드
    
    REST API 설계 시 가장 중요한 항목은 다음의 2가지로 요약할 수 있습니다.
    
    **첫 번째,** URI는 정보의 자원을 표현해야 한다.**두 번째,** 자원에 대한 행위는 HTTP Method(GET, POST, PUT, DELETE)로 표현한다.
    
    다른 것은 다 잊어도 위 내용은 꼭 기억하시길 바랍니다.
    
    REST는 Representational State Transfer의 줄임말
    
    API 또는 [애플리케이션 프로그래밍 인터페이스(Application Programming Interface)](https://www.redhat.com/ko/topics/api)
    는 애플리케이션 소프트웨어를 구축하고 통합하는 정의 및 프로토콜 세트입니다. 때때로 API는 정보 제공자와 정보 사용자 간의 계약으로 지칭되며 소비자에게 필요한 콘텐츠(호출)와 생산자에게 필요한 콘텐츠(응답)를 구성합니다. 예를 들어 날씨 서비스용 API에서는 사용자는 우편번호를 제공하고, 생산자는 두 부분(첫 번째는 최고 기온, 두 번째는 최저 기온)으로 구성된 응답으로 답하도록 지정할 수 있습니다.
    
    API가 RESTful로 간주되려면 다음 기준을 따라야 합니다.
    
    - 클라이언트, 서버 및 리소스로 구성되었으며 요청이 HTTP를 통해 관리되는 클라이언트-서버 아키텍처
    - [스테이트리스(stateless)](https://www.redhat.com/ko/topics/cloud-native-apps/stateful-vs-stateless) 클라이언트-서버 커뮤니케이션: 요청 간에 클라이언트 정보가 저장되지 않으며, 각 요청이 분리되어 있고 서로 연결되어 있지 않음
    - 클라이언트-서버 상호 작용을 간소화하는 캐시 가능 데이터
    - 정보가 표준 형식으로 전송되도록 하기 위한 구성 요소 간 통합 인터페이스. 여기에 필요한 것은 다음과 같습니다.
        - 요청된 리소스가 식별 가능하며 클라이언트에 전송된 표현과 분리되어야 합니다.
        - 수신한 표현을 통해 클라이언트가 리소스를 조작할 수 있어야 합니다(이렇게 할 수 있는 충분한 정보가 표현에 포함되어 있기 때문).
        - 클라이언트에 반환되는 자기 기술적(self-descriptive) 메시지에 클라이언트가 정보를 어떻게 처리해야 할지 설명하는 정보가 충분히 포함되어야 합니다.
        - 하이퍼미디어: 클라이언트가 리소스에 액세스한 후 하이퍼링크를 사용해 현재 수행 가능한 기타 모든 작업을 찾을 수 있어야 합니다.
    - 요청된 정보를 검색하는 데 관련된 서버(보안, 로드 밸런싱 등을 담당)의 각 유형을 클라이언트가 볼 수 없는 계층 구조로 체계화하는 계층화된 시스템.
    - 코드 온디맨드(선택 사항): 요청을 받으면 서버에서 클라이언트로 실행 가능한 코드를 전송하여 클라이언트 기능을 확장할 수 있는 기능.
    
    ### **REST의 장단점**
    
    장점
    
    - HTTP 프로토콜의 인프라를 그대로 사용하므로 REST API 사용을 위한 별도의 인프라를 구출할 필요가 없다.
    - HTTP 프로토콜의 표준을 최대한 활용하여 여러 추가적인 장점을 함께 가져갈 수 있게 해 준다.
    - HTTP 표준 프로토콜에 따르는 모든 플랫폼에서 사용이 가능하다.
    - Hypermedia API의 기본을 충실히 지키면서 범용성을 보장한다.
    - REST API 메시지가 의도하는 바를 명확하게 나타내므로 의도하는 바를 쉽게 파악할 수 있다.
    - 여러 가지 서비스 디자인에서 생길 수 있는 문제를 최소화한다.
    - 서버와 클라이언트의 역할을 명확하게 분리한다.
    
    단점
    
    - 표준이 자체가 존재하지 않아 정의가 필요하다.
    - 사용할 수 있는 메소드가 4가지밖에 없다.
    - HTTP Method 형태가 제한적이다.
    - 브라우저를 통해 테스트할 일이 많은 서비스라면 쉽게 고칠 수 있는 URL보다 Header 정보의 값을 처리해야 하므로 전문성이 요구된다.
    - 구형 브라우저에서 호환이 되지 않아 지원해주지 못하는 동작이 많다.(익스폴로어)
    
    ### **REST API 설계 예시**
    
    **1. URI는 동사보다는 명사를, 대문자보다는 소문자를 사용하여야 한다.**
    
    > Bad Example http://khj93.com/Running/
    > 
    > 
    > Good Example  http://khj93.com/run/
    > 
    
    **2. 마지막에 슬래시 (/)를 포함하지 않는다.**
    
    > Bad Example http://khj93.com/test/
    > 
    > 
    > Good Example  http://khj93.com/test
    > 
    
    **3. 언더바 대신 하이폰을 사용한다.**
    
    > Bad Example http://khj93.com/test_blog
    > 
    > 
    > Good Example  http://khj93.com/test-blog
    > 
    
    **4. 파일확장자는 URI에 포함하지 않는다.**
    
    > Bad Example http://khj93.com/photo.jpg
    > 
    > 
    > Good Example  http://khj93.com/photo
    > 
    
    **5. 행위를 포함하지 않는다.**
    
    > Bad Example http://khj93.com/delete-post/1
    > 
    > 
    > Good Example  http://khj93.com/post/1
    > 
    
    ref) [https://meetup.toast.com/posts/92](https://meetup.toast.com/posts/92)
    
    [https://khj93.tistory.com/entry/네트워크-REST-API란-REST-RESTful이란](https://khj93.tistory.com/entry/%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC-REST-API%EB%9E%80-REST-RESTful%EC%9D%B4%EB%9E%80)
    
    [https://www.redhat.com/ko/topics/api/what-is-a-rest-api](https://www.redhat.com/ko/topics/api/what-is-a-rest-api)
    
- 프레임워크 템플릿 분석해보기