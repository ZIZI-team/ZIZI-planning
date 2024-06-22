### CI/CD 구축 계획 및 일정

CI/CD 파이프라인 구축을 위한 계획과 일정을 아래와 같이 구성할 수 있습니다. 이 계획은 Google Play Store와 Apple App Store에 앱을 자동 배포하는 것을 목표로 합니다.

[Google playstore git action ci/cd](https://jsieun73.tistory.com/183)
[Apple store git action ci/cd](https://dev-in-gym.tistory.com/197)
<br>

#### 프레임워크 및 서비스 추천
```
    1. GitHub Actions
    - GitHub 레포지토리와 통합되어 있는 CI/CD 도구
    - 다양한 빌드 및 배포 작업을 자동화

    2. Fastlane
    - iOS 및 Android 앱 배포 자동화 도구
    - 코드 서명, 스토어 배포 등 다양한 기능 제공

    3. Google Play API
    - Google Play Store와의 연동을 위한 API
    - APK 업로드, 배포 관리 등 기능 제공

    4. Apple Developer API
    - Apple App Store와의 연동을 위한 API
    - IPA 업로드, 배포 관리 등 기능 제공
```
<br>

#### 전체 일정

| Week       | Task                                      |
|------------|-------------------------------------------|
| Week 1   | 레포지토리 설정, 계정 및 프로젝트 설정   |
| Week 2   | 파이프라인 설계 및 시크릿 관리            |
| Week 3~5   | Google Play Store 및 Apple App Store 배포 설정 |
| Week 6~7   | CI/CD 파이프라인 테스트 및 검증           |
| Week ~  | 운영 환경 설정 및 지속적인 모니터링       |

<br>

#### 1. **준비 단계 (Week 1)**

1. **레포지토리 설정**
- GitHub 레포지토리 생성
    - 소스 코드 및 관련 파일을 저장할 GitHub 레포지토리 생성
- 폴더 구조 정리
    - 앱 소스 코드, 빌드 스크립트, 구성 파일 등을 체계적으로 정리

2. **계정 및 프로젝트 설정**
- Google Play Console
    - Google Play 개발자 계정 생성 및 프로젝트 설정
- Apple Developer
    - Apple 개발자 계정 생성 및 프로젝트 설정

3. **도구 설치 및 환경 설정**
- git 자동 push 환경 설정 (매일 6시간마다)
- Fastlane
    - Fastlane 설치 및 기본 설정 완료

#### 2. **CI/CD 파이프라인 설계 (Week 2)**

1. **파이프라인 설계**
- 빌드 단계
    - 소스 코드 빌드 및 테스트
- 배포 단계
    - Google Play Store 및 Apple App Store에 배포 설정

2. **시크릿 관리**
- GitHub Secrets
    - 필요한 시크릿 (API 키, 인증서 등)을 GitHub Secrets에 저장

3. **워크플로우 파일 작성**
- Google Play Store 배포 워크플로우 작성
- Apple App Store 배포 워크플로우 작성

#### 3. **CI/CD 파이프라인 구현 (Week 3-5)**

1. **Google Play Store 배포**
- 빌드 스크립트 작성
- 배포 설정
    - Google Play API와 연동하여 APK 파일 업로드

2. **Apple App Store 배포**
- 빌드 스크립트 작성
- 배포 설정
    - Apple Developer API와 연동하여 IPA 파일 업로드

#### 4. **테스트 및 검증 (Week 6~7)**

1. **CI/CD 파이프라인 테스트**
- 테스트 케이스 작성
- 자동화된 빌드 및 배포 테스트

2. **이슈 해결 및 최적화**
- 테스트 과정에서 발견된 이슈 해결
- 파이프라인 최적화

#### 5. **운영 및 모니터링 ~**

1. **운영 환경 설정**
- 운영 중 발생할 수 있는 이슈 대응 계획 수립
- 모니터링 도구 설정

2. **지속적인 모니터링 및 유지보수**
- CI/CD 파이프라인 모니터링
- 주기적인 파이프라인 점검 및 유지보수

