🌐 Webbizcraftshop : AWS 기반 SiteBuilder 서비스
---
### 📍백엔드 팀원 소개
|                               [김시우](https://github.com/IpekoGosu)                                |                                            [김민우](https://github.com/minwoo1999)                                            |                               [박지호](https://github.com/pjho4746)                                |                               [이종수](https://github.com/leejongsuu)                                |
|:-----------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------:|
|                                       samuelk2873@gmail.com                                        |                                     hmg5959@gmail.com                                      |                                       pjho4746@gmail.com                                        |                                                    tjsdk34549@gmail.com                                                |
| <img src="https://github.com/CloudService-mobile-app/backend/assets/126854628/d628f11a-c30f-408d-9c30-35dc259e6075" width="150" height="150"> | <img src="https://github.com/CloudService-mobile-app/backend/assets/126854628/cfd64afa-d8f8-4d6d-9e3b-e2bf7f5d7ee4" width="150" height="150"> | <img src="https://github.com/CloudService-mobile-app/backend/assets/126854628/1aa8f1cc-cda9-4fa4-b460-1ec802567917" width="150" height="150"> | <img src="https://github.com/CloudService-mobile-app/backend/assets/126854628/eb420fb9-c7c1-4b1c-8762-c86110f53508" width="150" height="150"> |

### 📍개요
클라우드 기반의 혁신적인 플랫폼으로, AWS를 활용하여 손쉽게 고유한 웹사이트를 구축할 수 있습니다.

URL을 직접 지정하고 이미지를 업로드하여 자신만의 웹사이트를 만들 수 있으며, 방문자 수, 방문 횟수, 스토리지 용량, 트래픽과 같은 주요 지표를 실시간으로 모니터링하여 비즈니스 성과를 추적할 수 있습니다.

**보안상의 이유로 코드는 공개되지 않습니다.*

---
### 📍주요 기능
| 기능 | 설명                                                                              |
|---|---------------------------------------------------------------------------------|
| 고유한 웹사이트 구축 | 사용자들은 총 3개의 웹사이트를 생성할 수 있으며, 각 웹사이트는 직접 지정한 고유한 URL과 업로드한 이미지를 통해 자신만의 웹사이트를 만들 수 있습니다. |
| 클라우드 기반 플랫폼 | AWS의 S3, Route 53, CloudFront, ACM을 활용하여 동적 도메인을 생성합니다.        |
| 방문자 및 방문 횟수 추적 | 각 웹사이트에 방문한 방문자 수와 방문 횟수를 실시간으로 추적할 수 있습니다.                                     |
| 스토리지 용량 모니터링 | AWS CloudWatch를 통해 각 웹사이트의 스토리지 용량을 실시간으로 모니터링하여 사용자가 데이터를 얼마나 저장하고 있는지를 파악할 수 있습니다. |
| 트래픽 제한 | Bucket4j와 Redis(Lettuce)를 활용한 AOP를 통해 각 웹사이트의 트래픽을 100MB 아래로 제한하여 서버 부하를 관리합니다. |
| 실시간 트래픽 모니터링 및 알림 | AWS CloudWatch를 통해 트래픽이 100MB를 넘으면 알림이 가도록 설정하여 실시간으로 모니터링하고 대응합니다. |

---
### 📍 활동
**시작일** <br>
*2024.05.03* <br>

**1차 출시** <br>
*2024.06.14* <br>

---
### 📍 결과물
**배포 사이트** <br>
*https://main.webbizcraft.shop* <br>

**시연 영상** <br>
[1차 출시](https://drive.google.com/file/d/10inKFQjI8fsM7oqXdLQUS53h_G6_GTfK/view?usp=sharing)

---

### 📍 아키텍쳐 
![모바일앱협동조합 (4)](https://github.com/CloudService-mobile-app/backend/assets/126854628/ca51f232-19d7-4608-ab8f-34cf60bf3924)

---

### 📍 사용 기술스택
- SpringBoot
- JPA
- MySQL
- Redis
- AWS
    - EC2
    - S3
    - CloudFront
    - Route53
    - CloudWatch
- Docker
- Bucket4j
- Lettuce
- Nginx
- Jenkins

---

### 📍 사용 라이브러리
- Spring Boot Starter
- JWT
- Swagger
- Firebase
- OkHttp
- QueryDSL
- Lombok
- Jackson
- AWS SDK
    - CloudWatch
    - Route53
    - CloudFront
    - S3
- Database
    - H2
    - MySQL Connector
- Redis
    - Redisson
    - Embedded Redis
    - Bucket4j Core
    - Bucket4j Redis
- Logging
    - Discord Appender

---

### 📍프로젝트 구조
```
└── 🗂 main
    ├── 🗂 java
    │   └── 🗂 com
    │       └── 🗂 example
    │           └── 🗂 cloudservice
    │               ├── 📑 CloudServiceApplication.java
    │               ├── 🗂 auth
    │               │   ├── 🗂 cookie 
    │               │   │   └── 📑 CookieUtil.java
    │               │   ├── 🗂 entity 
    │               │   │   └── 📑 RefreshToken.java
    │               │   ├── 🗂 jwt 
    │               │   │   ├── 📑 JwtAuthenticationFilter.java    
    │               │   │   ├── 📑 JwtAuthorizationFilter.java   
    │               │   │   ├── 📑 JwtProvider.java       
    │               │   │   ├── 📑 MemberDetails.java   
    │               │   │   └── 📑 MemberDetailsService.java   
    │               │   ├── 🗂 repository
    │               │   │   └── 📑 RefreshTokenRepository.java
    │               │   ├── 🗂 service
    │               │   │   └── 📑 RefreshTokenService.java    
    │               │   └── 📑 MemberRole.java           
    │               ├── 🗂 cofig 
    │               │   ├── 🗂 Bucket4j 
    │               │   │   └── 📑 TokenBucketResolver.java 
    │               │   ├── 🗂 CloudWatch 
    │               │   │   └── 📑 CloudWatchConfig.java   
    │               │   ├── 🗂 jpa 
    │               │   │   └── 📑 JpaAuditingConfig.java
    │               │   ├── 🗂 mail 
    │               │   │   └── 📑 MailConfig.java
    │               │   ├── 🗂 RateLimit 
    │               │   │   ├── 📑 RateLimitAspect.java   
    │               │   │   └── 📑 RateLimiterConfig.java     
    │               │   ├── 🗂 redis
    │               │   │   ├── 📑 RedisCacheConfig.java   
    │               │   │   └── 📑 RedisConfig.java   
    │               │   ├── 🗂 redisson
    │               │   │   └── 📑 RedissonConfig.java
    │               │   ├── 🗂 s3
    │               │   │   ├── 📑 awstest.java   
    │               │   │   └── 📑 S3Config.java     
    │               │   ├── 🗂 security
    │               │   │   ├── 📑 SecurityConfig.java   
    │               │   │   └── 📑 SecurityUtils.java   
    │               │   └── 🗂 swagger
    │               │       └── 📑 SwaggerConfig.java  
    │               ├── 🗂 global 
    │               │   ├── 🗂 base 
    │               │   │   └── 📑 BaseTimeEntity.java
    │               │   ├── 🗂 common 
    │               │   │   └── 📑 CommonResDto.java
    │               │   ├── 🗂 dto
    │               │   │   ├── 📑 CommonResponse.java   
    │               │   │   └── 📑 ErrorResponse.java  
    │               │   ├── 🗂 error
    │               │   │   ├── 📑 BucketCapacityException.java 
    │               │   │   ├── 📑 DuplicateAccountException.java 
    │               │   │   ├── 📑 DuplicateUrlException.java           
    │               │   │   ├── 📑 EncryptException.java 
    │               │   │   ├── 📑 FileTooLargeException.java 
    │               │   │   ├── 📑 InvalidTokenException.java   
    │               │   │   ├── 📑 NotFoundAccountException.java 
    │               │   │   ├── 📑 PasswordNotMatchException.java 
    │               │   │   ├── 📑 S3UploadException.java  
    │               │   │   ├── 📑 UnAuthorizedException.java 
    │               │   │   ├── 📑 WebsiteLimitException.java           
    │               │   │   └── 📑 WebsiteNotFoundException.java  
    │               │   ├── 🗂 log
    │               │   │   ├── 📑 FilterConfig.java   
    │               │   │   └── 📑 MDCFilter.java 
    │               │   ├── 📑 ErrorCodes.java  
    │               │   ├── 📑 ErrorResponse.java  
    │               │   ├── 📑 GlobalExceptionHandler.java  
    │               │   └── 📑 GlobalExceptionHandlerFilter.java          
    │               ├── 🗂 member 
    │               │   ├── 🗂 application
    │               │   │   ├── 🗂 dto
    │               │   │   │    ├──📑 MemberResponseDto.java     
    │               │   │   │    └──📑 MemeberRequestDto.java       
    │               │   │   └── 🗂 impl
    │               │   │   │    ├──📑 MailServiceImpl.java     
    │               │   │   │    ├──📑 MemberServiceImpl.java
    │               │   │   │    └──📑 MiddleTableServiceImpl.java      
    │               │   │   ├── 📑 MemberService.java  
    │               │   │   └── 📑 MiddleTableService.java        
    │               │   ├── 🗂 domain
    │               │   │   ├── 🗂 repository
    │               │   │   │    ├──📑 MemberRepository.java     
    │               │   │   │    └──📑 MiddleTableRepository.java   
    │               │   │   ├── 📑 Member.java  
    │               │   │   └── 📑 MiddleTable.java       
    │               │   ├── 🗂 exception
    │               │   │   └── 🗂 dto
    │               │   │        ├──📑 CommonResDto.java     
    │               │   │        └──📑 CommonResponse.java 
    │               │   ├── 🗂 presentation
    │               │   │   └── 📑 MemberController.java
    │               │   ├── 🗂 restapi
    │               │   │   └── 📑 MemberApi.java
    │               │   └── 🗂 utils
    │               │       ├── 📑 MemberScheduler.java
    │               │       └── 📑 MemberUtils.java   
    │               ├── 🗂 visit 
    │               │   ├── 🗂 application  
    │               │   │   └── 🗂 dto
    │               │   │   │    └──📑 VisitResponseDto.java   
    │               │   │   └── 🗂 impl
    │               │   │   │    ├──📑 VisitRedisService.java     
    │               │   │   │    └──📑 VisitServiceImpl.java    
    │               │   │   └── 📑 VisitService.java       
    │               │   ├── 🗂 domain
    │               │   │   ├── 🗂 repository    
    │               │   │   │    ├──📑 VisitRepository.java 
    │               │   │   │    ├──📑 VisitRepositoryImpl.java 
    │               │   │   │    └──📑 VisitRepositoryJPA.java   
    │               │   │   └── 📑 Visit.java    
    │               │   ├── 🗂 exception
    │               │   │   ├── 🗂 dto
    │               │   │   │    ├──📑 CommonResponse.java     
    │               │   │   │    └──📑 RateLimiterException.java 
    │               │   ├── 🗂 presentation
    │               │   │   └── 📑 VisitController.java
    │               │   ├── 🗂 restapi
    │               │   │   └── 📑 VisitApi.java
    │               │   └── 🗂 scheduler
    │               │       └── 📑 VisitScheduler.java
    │               └── 🗂 websiteaa 
    │                   ├── 🗂 application
    │                   │   ├── 🗂 dto
    │                   │   │    ├──📑 WebsiteaaRequestDto.java     
    │                   │   │    └──📑 WebsiteaaResponseDto.java       
    │                   │   └── 🗂 impl
    │                   │   │    └──📑 WebsiteaaServiceImpl.java      
    │                   │   └── 📑 WebsiteaaService.java        
    │                   ├── 🗂 domain
    │                   │   ├── 🗂 repository    
    │                   │   │    └──📑 WebsiteaaRepository.java   
    │                   │   ├── 📑 Template.java  
    │                   │   └── 📑 Websiteaa.java       
    │                   ├── 🗂 exception
    │                   │   └── 🗂 dto
    │                   │        └──📑 CommonResponse.java 
    │                   ├── 🗂 presentation
    │                   │   └── 📑 WebsiteaaController.java
    │                   ├── 🗂 restapi
    │                   │   └── 📑 WebsiteaaApi.java
    │                   └── 🗂 utils
    │                       │── 📑 MultipartJackson2HttpMessageConverter.java   
    │                       │── 📑 WebsiteaaEnums.java         
    │                       └── 📑 WebsiteaaUtils.java 
    └── 🗂 resources
         └── 🗂 scripts   
         │   ├── 📑 getVisitCounts.lua
         │   └── 📑 incrementVisitCount.lua   
         └── 🗂 temlates   
         │   ├── 📑 bizcraft_logo.png
         │   └── 📑 email-template.html          
         ├── 📑 application.yaml      
         ├── 📑 application-dev.yml      
         ├── 📑 application-local.yml      
         ├── 📑 application-prod.yml  
         ├── 📑 application-test.yml
         └── 📑 logback.xml  
                                        
```
---

### commit message convention
- feat: 새로운 기능 추가
- fix: 버그 수정
- docs: 문서
- style: 포맷팅, 누락된 세미콜론 등
- refactor: 코드 리팩토링
- test: 테스트 관련
- chore: 기타 수정
- build: 빌드 시스템 또는 외부 의존성에 영향을 주는 변경
- remove: 파일을 삭제
