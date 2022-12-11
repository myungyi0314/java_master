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

