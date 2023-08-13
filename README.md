
#  카카오 쇼핑하기 (클론 프로젝트) 

<div align="left">

<img width="400" alt="스크린샷 2023-08-13 오후 5 38 40" src="https://github.com/rnjsgo/kakao-clone-project-deploy/assets/102651155/71053379-70e1-4de9-8bd7-b6bd606ba627">

</div>


> **카카오 테크 캠퍼스 과정 2단계 (카카오 쇼핑하기 클론 프로젝트)** <br/> **개발기간: 2023.06.26 ~ 2023.08.04**


## 프로젝트 소개

 본 프로젝트는 카카오 테크 캠퍼스 과정 2단계 - 카카오 쇼핑하기 백엔드 클론 프로젝트이다.<br>
 총 6주차 과정으로 진행되었으며, 각 주차별 프로젝트 진행 내용은 다음과 같다.<br>

### 1주차
```
1. 요구사항분석/API요청 및 응답 시나리오 분석
2. 요구사항 추가 반영 및 테이블 설계도
```



### 2주차
```
1. 전체 API 주소 설계
2. Mock API Controller 구현
```


### 3주차


```
레포지토리 단위테스트
```

### 4주차
```
컨트롤러 단위 테스트
```

### 5주차

```
코드 리팩토링
```

### 6주차

```
카카오 클라우드 배포
```

<br><br>
본 레포지토리는 개인 배포용 레포지토리이다.<br>
**원본**
https://github.com/Kakao-tech-campus-BE/step2-BE-kakao-shop

## Stacks 🐈

![spring](https://img.shields.io/badge/spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![mysql](https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![kakaocloud](https://img.shields.io/badge/kakao_Cloud-FFCD00?style=for-the-badge&logo=kakao%20Meet&logoColor=white)
<br>
![notion](https://img.shields.io/badge/notion-000000?style=for-the-badge&logo=notion&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=Git&logoColor=white)


---
## 화면 구성 📺
| 메인 화면  |  회원가입   | 로그인 |
| :-------------------------------------------: | :------------: |:------------: |
| <img width="500" height="400" src="https://github.com/rnjsgo/kakao-clone-project-deploy/assets/102651155/f551cfde-6e81-4966-a91f-65c7e7b03e27"/>  |  <img width="500" height="400" src="https://github.com/rnjsgo/kakao-clone-project-deploy/assets/102651155/d80fa8a4-b234-4c7b-8d5e-9f06084d8a1c"/>|<img width="500" height="400" src="https://github.com/rnjsgo/kakao-clone-project-deploy/assets/102651155/5bb1d211-2f0e-49ca-be6e-1765b2fbc9b7"/>  
| 상품 화면  |  장바구니  |  결제 화면 |
| <img width="500" height="400" src="https://github.com/rnjsgo/kakao-clone-project-deploy/assets/102651155/decc83b9-b739-45ab-b952-56e8fd15aabd"/>   | <img width="500" height="400" src="https://github.com/rnjsgo/kakao-clone-project-deploy/assets/102651155/a69c55ac-535d-4161-bbe9-2ee98e283f30"/>  |<img width="500" height="400" src="https://github.com/rnjsgo/kakao-clone-project-deploy/assets/102651155/2c098255-bfb6-4e91-a80f-ad5d6a4edadf"/>



## 시연 영상 <br>
https://www.youtube.com/watch?v=jPSOM2gf_kY&ab_channel=UNS<br>

---
## 아키텍쳐

### 디렉토리 구조
```.
├── Dockerfile
├── README.md
├── backup-data-v2
│   ├── api-pdf.pdf
│   ├── data.sql
│   ├── schema.sql
│   ├── 카카오톡 쇼핑하기_화면설계서.pdf
│   └── 카카오테크캠퍼스_API 명세서_초안.docx
├── bin
├── build
├── build.gradle
├── gradle
│   └── wrapper
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
├── gradlew
├── images
├── settings.gradle
├── src
│   ├── docs
│   │   └── asciidoc
│   │       └── api-docs.adoc
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── example
│   │   │           └── kakao
│   │   │               ├── KakaoApplication.java
│   │   │               ├── _core
│   │   │               │   ├── errors
│   │   │               │   │   ├── GlobalExceptionHandler.java
│   │   │               │   │   ├── GlobalValidationHandler.java
│   │   │               │   │   └── exception
│   │   │               │   │       ├── Exception400.java
│   │   │               │   │       ├── Exception401.java
│   │   │               │   │       ├── Exception403.java
│   │   │               │   │       ├── Exception404.java
│   │   │               │   │       └── Exception500.java
│   │   │               │   ├── security
│   │   │               │   │   ├── CustomUserDetails.java
│   │   │               │   │   ├── CustomUserDetailsService.java
│   │   │               │   │   ├── JWTProvider.java
│   │   │               │   │   ├── JwtAuthenticationFilter.java
│   │   │               │   │   └── SecurityConfig.java
│   │   │               │   └── utils
│   │   │               │       ├── ApiUtils.java
│   │   │               │       ├── FakeStore.java
│   │   │               │       └── FilterResponseUtils.java
│   │   │               ├── cart
│   │   │               │   ├── Cart.java
│   │   │               │   ├── CartJPARepository.java
│   │   │               │   ├── CartRequest.java
│   │   │               │   ├── CartResponse.java
│   │   │               │   ├── CartRestController.java
│   │   │               │   └── CartService.java
│   │   │               ├── log
│   │   │               │   ├── ErrorLog.java
│   │   │               │   └── ErrorLogJPARepository.java
│   │   │               ├── order
│   │   │               │   ├── Order.java
│   │   │               │   ├── OrderJPARepository.java
│   │   │               │   ├── OrderResponse.java
│   │   │               │   ├── OrderRestController.java
│   │   │               │   ├── OrderService.java
│   │   │               │   └── item
│   │   │               │       ├── Item.java
│   │   │               │       └── ItemJPARepository.java
│   │   │               ├── product
│   │   │               │   ├── Product.java
│   │   │               │   ├── ProductJPARepository.java
│   │   │               │   ├── ProductResponse.java
│   │   │               │   ├── ProductRestController.java
│   │   │               │   ├── ProductService.java
│   │   │               │   └── option
│   │   │               │       ├── Option.java
│   │   │               │       └── OptionJPARepository.java
│   │   │               └── user
│   │   │                   ├── User.java
│   │   │                   ├── UserJPARepository.java
│   │   │                   ├── UserRequest.java
│   │   │                   ├── UserResponse.java
│   │   │                   ├── UserRestController.java
│   │   │                   └── UserService.java
│   │   └── resources
│   │       ├── application-ide.yml
│   │       ├── application-local.yml
│   │       ├── application-prod.yml
│   │       ├── application-test.yml
│   │       ├── application.yml
│   │       ├── db
│   │       │   └── teardown.sql
│   │       └── static
│   │           └── docs
│   │               └── api-docs.html
│   └── test
│       └── java
│           └── com
│               └── example
│                   └── kakao
│                       ├── MyRestDoc.java
│                       ├── _core
│                       │   ├── regex
│                       │   │   └── RegexTest.java
│                       │   └── util
│                       │       └── DummyEntity.java
│                       ├── cart
│                       │   └── CartRestControllerTest.java
│                       ├── order
│                       │   └── OrderRestControllerTest.java
│                       ├── product
│                       │   └── ProductRestControllerTest.java
│                       └── user
│                           └── UserRestControllerTest.java
└── startFront.sh
```
### ERD (Entity Relationship Diagram)
<img width="600" alt="image" src="https://github.com/rnjsgo/kakao-clone-project-deploy/assets/102651155/f9673c58-eef7-40c5-bc74-f23b74111d31">





