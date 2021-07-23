## 스프링 부트 실습을 위한 저장소 

# 프로젝트 설명
스프링 부트 실습을 위한 저장소입니다. 네이버 부스트 코스 풀스택 개발자 과정을 통하여 스프링 MVC 전반을 학습하였습니다. 이제 스프링 부트를 이용, 백엔드를 구축하는 연습을 하려고 합니다. 

# 환경 및 세팅

* 프로젝트: 메이븐 프로젝트
* 언어: 자바 1.8
* 스프링 부트: 2.5.3
* 의존성: 스프링 웹

# 코드 및 사용법 

* demo
    * 'src/main/java/com/example/demo/DemoApplication.java' 컨트롤러 코드에 대한 설명입니다.
    * 'hello()' 메소드는 리퀘스트로부터 'name' 파라미터를 받아서 출력하는 메소드입니다. 
    * '@GetMapping(“/hello”)' 어노테이션을 통하여 'hello' 메소드가 'http://localhost:8080/hello'로 보내진 요청에 응답하도록 합니다.  
    * 'name' 파라미터가 없다면 기본값은 World입니다.
    * './mvnw spring-boot:run' 명령어를 통하여 윈도우즈와 맥 모두 동작합니다. IDE에서 DemoApplication.java를 Run 해도 잘 동작합니다.
    * 'http://localhost:8080/heloo' 로 접속하면 'Hello World!' 혹은 'Hello {name}!' 가 출력됩니다.

* rest-service
    * 'src/main/java/com/example/restservice/Greeting.java'에 '/greeting' 에서 'GET' 요청을 처리하는 웹서비스를 구현합니다.
    * 'src/main/java/com/example/restservice/GreetingController.java'에 HTTP 요청을 처리할 컨트롤러를 구현한다. 'Greeting' 클래스의 새로운 인스턴스를 '/greeting'의 'GET' 요청을 처리한다. 
    * '@GetMapping' 어노테이션을 통하여 '/greeting'으로 들어온 HTTP 'GET' 요청을 'greeting()' 메소드에 연결한다.
    * '@RequestParam' 어노테이션은 쿼리 문자열 파라미터 'name'의 값을 'greeting()' 메소드의 'name' 파라미터로 묶는다. 
    * MVC 컨트롤러와 RESTful web service 컨트롤러는 HTTP 응답 바디가 만들어지는 방식에서 다르다. view 기술을 사용하여 greeting 데이터를 HTML로 렌더링하는 것과는 달리, RESTful 웹 서비스 컨트롤러는 Greeting 객체를 채워서 리턴되고, 즉시 HTTP로 json의 형태로 응답된다.
    * 스프링의 ' MappingJackson2HttpMessageConverter' 가 자동적으로 'Greeting' 인스턴스를 JSON으로 변환해준다. 
    * Maven을 사용하므로 './mvnw spring-boot:run' 으로 어플리케이션을 실행할수 있다. 또한 './mvnw clean package' 명령어로 JAR 파일을 빌드한 뒤, 'java -jar target/gs-rest-service-0.1.0.jar' 명령어로 JAR 파일을 실행할 수도 있다. 
    * 'http://localhost:8080/greeting' 로 접속하면 '{"id":1,"content":"Hello, World!"}' 가 출력된다. 
