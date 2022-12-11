## STEP1 스프링부트 프로젝트 생성
[Spring Initializr Link](https://start.spring.io/)

SpringBoot 프로젝트를 setting

![image](https://user-images.githubusercontent.com/52149400/206891437-c212a47a-eb1a-4949-9b90-2395e4ac402f.png)

## STEP2 
### Project
- 빌드관리 도구를 선택 ( Gradle을 이용하여 개발하는 추세 )
  - 스크립트의 가독성이 좋고, 빌드와 테스트 실행결과가 gradle이 더 빠르다. gradle은 캐시를 사용하여 이미 업데이트된 것에 대해서는 작업이 실행되지 않아 빌드시간이 단축
- 각종 라이브러리들을 버전, 종속성 등을 명시하여 사용
- 라이브러리들의 의존관계들을 모두 가져와 의존관계를 관리 

### SpringBoot
- SpringBoot의 버전을 선택
- **SNAPSHOT**은 개발중인 버전,  **M1**은 정식으로 릴리즈 되지 않은 버전
- 사용할 때는 버전 숫자 뒤에 영어가 붙어있지 않는 것으로

### Project Metadata

|  🐋| 🐳 |
| -- | -- | 
|Group | 	보통 기업의 도메인명을 기입한다.<br/>개인 프로젝트라면 블로그도메인이나 자유롭게 만들면 된다.<br/>(ex: com.myungyi )|
|Artifact | 	빌드된 결과물 이름을 의미한다. |
|Name |프로젝트명이다. |
|Description | 프로젝트 관련 설명을 간단히 작성한다.|
|Package name | 	패키지명이다. <br/>( ex: com.myungyi.hello)|
|Packaging | 배포 형태 설정<br/><br/>[ jar ] >> Java 어플리케이션이 동작할 수 있도록 프로젝트를 압축한 파일로, class와 라이브러리파일이 포함되어 있다. 그리고 JRE만 있어도 실행할 수 있다. 서버에서 java -jar hello.jar하면 실행가능<br/><br/>[ war ] >> Servlet, Jsp 컨테이너를 배치할 수 있는 웹 어플리케이션을 압축한 파일이다. 웹 프로젝트에는 jsp, html , javasscript등 웹과 관련된것들이 포함되어 있고, 웹서버나 was가 필요<br/><br/>웹화면이 필요한 어플리케이션은 war로 패키징하고 , api서버로 사용하는 것과 같이 사용한다면 java 프로젝트로만 동작하면 되기 때문에 jar로 하면 된다.    |
|Java | 사용하고자 하는 자바버전을 선택|


