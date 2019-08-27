이 체험은 다음과 같이 설명될 수 있습니다.

```
This auth starter implements withAuthenticator HOC to provide a basic authentication flow for signing up signing in users as well as protected client side routing using AWS Amplify.

Auth features: User sign up, User sign in, Multi-factor Authentication, User sign-out.
```

여기서 키워드는 'Auth features: User sign up, User sign in, Multi-factor Authentication, User sign-out.'인데, 보호된(protected) 클라이언트 사이드 라우팅과 사용자 로그인에 대한 기본적인 인증 흐름을 제공하는 기본 스타터 팩이라고 생각하시면 됩니다.

이를 위해 가장 먼저 진행할 예제는 다음과 같습니다(내용에 대한 출처는 [여기](https://github.com/aws-samples/create-react-app-auth-amplify)를 참고하시기 바랍니다).

> 만약 세미나가 진행되고 있다면, 앞에서 발표하는 진행자와 함께 다음을 진행하시면 됩니다!

이번 세션을 통해 완성될 결과물

[View Demo](https://master.d2ka7y7551sk8n.amplifyapp.com/)

![Amplify Auth](https://github.com/aws-samples/create-react-app-auth-amplify/raw/master/src/images/auth.gif)

## Run locally with the Amplify CLI(함께 진행할 때 추천, 아마톤 사전 세션에서 사용됩니다)

1. [create-react-app-auth-amplify](https://github.com/aws-samples/create-react-app-auth-amplify)에 접속한 후 자신의 계정으로 해당 레포지토리를 포크하세요. 포크한 다음에는 자신의 로컬 환경에 클론하세요.

```
git clone https://github.com/<username>/create-react-app-auth-amplify.git

cd create-react-app-auth-amplify && npm install
```

2. Amplify CLI를 사용하기 위한 사용자 계정을 설정합니다.

```
> amplify configure
Follow these steps to set up access to your AWS account:

Sign in to your AWS administrator account:
https://console.aws.amazon.com/

Press Enter to continue
// 로그인이 완료됐다면 엔터를 눌러주세요.

// 리전을 설정합니다(서울 리전은 'ap-southeast-2' 입니다.)
Specify the AWS Region
? region:  
  ap-northeast-1 
  ap-northeast-2 
  ap-southeast-1 
❯ ap-southeast-2 
  ap-south-1 
  us-east-1 
  us-east-2 
(Move up and down to reveal more choices)

? user name: amathon

// 열린 AWS 콘솔을 통해 유저를 생성합니다.
// 콘솔도 사용할 수 있으니 콘솔에 대한 설정도 추가,
// 권한은 원활한 실습을 위해  AdministratorAccess를 사용하지만, 실제로 사용할 때는 사용할 서비스에 대한 권한만 부여하는 것을 권장한다고 설명해야 함

// 액세스 키와 시크릿 키 화면이 보여지면 터미널로 돌아와 엔터를 누른 후 액세스 키와 시크릿 키를 입력하도록 한다.
Enter the access key of the newly created user:
? accessKeyId:  AKIA4HQ7D5**********
? secretAccessKey:  C4rJa4Q/2UJNA1Jcj6Fr********************
This would update/create the AWS Profile in your local machine
? Profile Name:  amathon
```

3. 만들어진 AWS 유저를 통해 amplify 적용하기

```
> amplify init
Note: It is recommended to run this command from the root of your app directory
? Enter a name for the environment amathonenv
? Choose your default editor: Visual Studio Code
Using default provider  awscloudformation

For more information on AWS Profiles, see:
https://docs.aws.amazon.com/cli/latest/userguide/cli-multiple-profiles.html

? Do you want to use an AWS profile? Yes
? Please choose the profile you want to use amathon
⠙ Initializing project in the cloud...

// 완료될 때까지 기다려줍니다(1분 정도 소요)
```

4. 현재 amplify의 상태 확인(관련 정보는 amplify 디렉터리에 저장됨)

```
> amplify status

Current Environment: amathonenv

| Category | Resource name   | Operation | Provider plugin   |
| -------- | --------------- | --------- | ----------------- |
| Auth     | cognitocf0c6096 | Create    | awscloudformation |

```

기본적으로 Auth가 적용되어 있기 때문에 상태에는 Auth가 설정되어 있습니다. 이때 사용되는 Auth는 인증과 관련된 서비스를 제공하는 Cognito를 뜻하고, 실제로 AWS 콘솔에서 Cognito가 연결된 것을 확인할 수 있습니다.

5. 클라우드에 업로드하기

```
> amplify push

...

✔ All resources are updated in the cloud
// 완료될 때까지 기다려줍니다(3분 정도 소요)
```

6. https 호스팅 추가하기

```
> amplify hosting add

? Select the environment setup: PROD (S3 with CloudFront using HTTPS)
? hosting bucket name amathon-hosting
? index doc for the website index.html
? error doc for the website index.html

You can now publish your app using the following command:
Command: amplify publish
```

7. 배포하기

```
> amplify publish

Current Environment: amathonenv

| Category | Resource name   | Operation | Provider plugin   |
| -------- | --------------- | --------- | ----------------- |
| Hosting  | S3AndCloudFront | Create    | awscloudformation |
| Auth     | cognitocf0c6096 | No Change | awscloudformation |
? Are you sure you want to continue? Yes
⠧ Updating resources in the cloud. This may take a few minutes...

// 오래 걸리기때문에 잠시 쉬는시간을 가지겠습니다.(15분 예정)
```

이제부터는 'amplify push'와 'amplify publish'를 이용하면 인프라를 세팅하고 배포할 수 있는 환경이 구성되었습니다. 앞으로는 내용이 변경되면 중단없이 앱을 변경할 수 있게 되었습니다. 축하드립니다!

## AWS Amplify Console을 이용한 시작(혼자 진행할 때 추천)

The AWS Amplify Console provides hosting for fullstack serverless web apps. [Learn more](https://console.amplify.aws). Deploy this app to your AWS account with a single click:

[![amplifybutton](https://oneclick.amplifyapp.com/button.svg)](https://console.aws.amazon.com/amplify/home#/deploy?repo=https://github.com/aws-samples/create-react-app-auth-amplify)

The Amplify Console will fork this repo in your GitHub account, and then build and deploy your backend and frontend in a single workflow. Your app will be available at `https://master.appid.amplifyapp.com`.

>>>>>>>>>> 권한 부여가 필요한데, 그에 대한 가이드가 없어서 추후 제공 예정(롤을 부여해야 제대로 작동합니다!)
>>>>>>>>>> 완료되면 상단의 'Learn how to get the most out of Amplify Console'를 참고해 각 내용을 진행해보는 것도 좋습니다.

```
// 현재 amplify 상태 확인
> amplify status
```

만약 여기서 추가적인 인증 구현(소셜 로그인 등)을 원하신다면 Checkout Nader Dabit's [Complete Guide to User Authentication](https://dev.to/dabit3/the-complete-guide-to-user-authentication-with-the-amplify-framework-2inh)을 참고하시길 바랍니다.

