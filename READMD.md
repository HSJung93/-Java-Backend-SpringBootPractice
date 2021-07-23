## 스프링 부트 실습을 위한 저장소 

# 프로젝트 설명
스프링 부트 실습을 위한 저장소입니다. 네이버 부스트 코스 풀스택 개발자 과정을 통하여 스프링 MVC 전반을 학습하였습니다. 이제 스프링 부트를 이용, 백엔드를 구축하는 연습을 하려고 합니다. 

# 환경 및 세팅

* 프로젝트: 메이븐 프로젝트
* 언어: 자바 1.8
* 스프링 부트: 2.5.3
* 의존성: 스프링 웹

# 코드 및 사용법 

* 'src/main/java/com/example/demo/DemoApplication.java' 컨트롤러 코드에 대한 설명입니다.
* 'hello()' 메소드는 리퀘스트로부터 'name' 파라미터를 받아서 출력하는 메소드입니다. 
* '@GetMapping(“/hello”)' 어노테이션을 통하여 'hello' 메소드가 'http://localhost:8080/hello'로 보내진 요청에 응답하도록 합니다.  
* 'name' 파라미터가 없다면 기본값은 World입니다.
* './mvnw spring-boot:run' 명령어를 통하여 윈도우즈와 맥 모두 동작합니다. IDE에서 DemoApplication.java를 Run 해도 잘 동작합니다.
