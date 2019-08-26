# Amplify로 풀사이클 개발 체험하기

여러분을 환영합니다! 만약 미리 진행하고 싶으시다면 세션의 흐름과 무관하게 먼저 실습을 진행하셔도 무방하니 자유롭게 세션을 즐겨주세요!

### 본 실습 세션의 기본적인 흐름은 아래와 같습니다.

- VS Code의 터미널에서 Amplify CLI를 이용해 유저 생성 및 AWS IAM 설정하기
- VS Code의 터미널에서 Amplify CLI를 이용해 생성한 유저의 엑세스 키 ID와 비밀 액세스 키 설정하기
- VS Code의 터미널에서 Create React App으로 웹 앱의 클라이언트 만들기
- VS Code의 터미널에서 Amplify CLI를 이용해 AWS Cognito 서비스 연결하기
- VS Code의 터미널에서 Amplify CLI를 이용해 AWS S3와 CloudFront를 구성해 서비스 호스팅하기

- 짜잔! 풀사이클 개발 환경 탄생!

# 필수 준비 사항

## 1. PC 또는 Mac

본 세션은 코딩 과정이 포함되어 있습니다. 또한 CLI(Command Line Interface) 조작이 꼭 필요합니다. 모바일 환경(iPhone, iPad, Android)에서는 진행이 불가능하니 꼭 PC/Mac 환경에서 진행하세요.

## 2. AWS 루트 계정

- AWS 계정 만들기 [이동](https://aws.amazon.com/ko/)

본 가이드는 한명이 하나의 AWS 계정을 사용한다고 가정합니다. AWS Route 53, S3, CloudFront, Certification Manager에 접근할 수 있어야 하며, 다른 사람과 계정을 공유하게되면 특정 리소스에 대해 충돌이 발생하므로 권장하지 않습니다.

본 워크샵의 일환으로 시작하는 모든 리소스는 AWS 계정이 12개월 미만인 경우, 제공하는 AWS 프리티어로 충분히 가능합니다.

만약의 경우 프리티어를 넘어 서비스를 이용하게 되면, 과금 될 수 있기 때문에 이 점을 유의하세요.

따라서, 새로운 실습용 계정을 만드시길 권장합니다. 자세한 내용은 [AWS 프리 티어 페이지](https://aws.amazon.com/free/)를 참조하세요.

## 3. 텍스트 에디터

- VS Code [다운로드](https://code.visualstudio.com/)

본 실습 세션에는 실제 코딩이 포함됩니다. VS Code를 꼭 설치해주세요.

## 4. Terminal & Amplify CLI

터미널에서 다음 명령어를 통해 설치를 진행하시면 됩니다. 만약 제대로 설치가 되지 않는다면, [여기](https://aws-amplify.github.io/docs/)를 참고하세요.

```
> npm install -g @aws-amplify/cli
> amplify configure
```

## 앞으로 진행될 목차

### [React와 Amplify로 풀사이클 개발 체험하기, 이론 자료 - Lectures](lectures/chapter1.md)

[What is learning today?](lectures/chapter1.md)
[What is Full Cycle and FCD(Full Cycle Developer)?](lectures/chapter2.md)
[What is Amplify?](lectures/chapter3.md)
[What is React?](lectures/chapter4.md)

[How to use Amplify in React?](lectures/chapter5.md)

### [React와 Amplify로 풀사이클 개발 체험하기, 실습 자료 - CodeLab](codelab/README.md)

### [실습에 사용되는 코드 샘플](code_sample/)
