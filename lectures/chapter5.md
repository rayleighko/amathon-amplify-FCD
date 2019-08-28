# How to use Amplify in React?

여기서는 실습을 통해 학습하게 될 Amplify와 리액트를 활용한 풀사이클 개발의 전체적인 흐름에 대해 설명할 예정입니다.

기본적으로 프론트엔드 로직은 모바일, 웹에서 사용하는 다양한 도구를 사용할 수 있지만, 오늘은 React를 통해 웹 프론트엔드를 구성할 예정입니다.

더불어 실습에 사용될 예제는 '[create-react-app-auth-amplify](https://github.com/aws-samples/create-react-app-auth-amplify)'을 사용해 구성할 예정이며, create-react-app-auth-amplify에서 제공하는 AWS Amplify 소개를 참고해 다음과 같이 소개될 수 있는 어플리케이션을 만들어보도록 하겠습니다.

```
The AWS Amplify Console provides continuous deployment and hosting for modern web apps (single page apps and static site generators) with serverless backends. The Amplify Console offers globally available CDNs, easy custom domain setup, feature branch deployments, and password protection.

1. Login to the Amplify Console here.
2. Connect your Create React App repo and pick a branch. If you're looking for a Create React App+Amplify starter, try the create-react-app-auth-amplify starter that demonstrates setting up auth in 10 minutes with Create React App.
3. The Amplify Console automatically detects the build settings. Choose Next.
4. Choose Save and deploy.

If the build succeeds, the app is deployed and hosted on a global CDN with an amplifyapp.com domain. You can now continuously deploy changes to your frontend or backend. Continuous deployment allows developers to deploy updates to their frontend and backend on every code commit to their Git repository.
```

마지막으로 Amplify의 기능들은 다음과 같으며, 이 중 별표(\*)가 붙은 도구를 이번 자료에서 사용할 예정입니다.

| Category      |
| ------------- |
| analytics     |
| api           |
| auth \*       |
| function      |
| hosting \*    |
| interactions  |
| notifications |
| storage       |
| xr            |

그렇다면 이제 본격적으로 [실습 진행하러 가기](../codelab/README.md)를 통해 실습을 진행하면서 Amplify로 풀사이클 개발을 체험해보도록 합시다! 당연하지만, '체험'이기 때문에 깊은 이야기를 하지는 않습니다. 만약 다음과 같은 질문이 떠오르신다면, 구글신의 힘을 빌어보도록 하죠(물론 대략적인 설명은 덧붙여놓겠습니다. ㅎㅎ)!

- Amplify를 통해 server side rendering을 구현하기 위해서는 어떻게 하면 좋을까요?

> Amplify 이전에 리액트로 server side rendering을 한다는 것은 두 가지 케이스로 나눠서 생각해볼 수 있습니다. Next와 같은 별도의 라이브러리를 사용하거나, 직접 서버 사이드 렌더링에 필요한 서버를 구성하는 방법이 그 두 케이스인데, 두 케이스 모두 빌드를 진행해 dist 디렉터리를 생성하게되고, 그 이후에는 dist를 ec2에 올려 직접 컴퓨팅하거나 Lambda와 같은 Faas를 통해 컴퓨팅을 AWS에 일임할 수 있습니다.

- Amplify를 실무에 적용하기 위해서는 어떤 지식이 필요할까요?

> Amplify가 아니더라도 어떤 도구를 사용하려 할 때 기본적인 지식을 모르고 사용하면 사이드 이펙트를 관리하기 어렵습니다. 만약 최대한 사이드 이펙트를 줄이고 싶으시다면, 기본적인 CS를 포함해 Cloud Computing과 클라이언트 구현 능력, 사용되는 AWS 도구들에 대한 지식 등이 필요하지 않을까요?

- Amplfiy를 쓴다고 해도 결국 AWS Console을 써야 하고, 에디터로 코드를 작성해야 한다면 굳이 왜 써야 할까요?

> 여기에 대한 답은 지극히 주관적일 수밖에 없기 때문에, 답할 수 없습니다. 하지만, 개발 과정에서 염두하고 사용하지 않는다면 굳이 Amplify를 써야하는 상황은 발생하지 않을 거라는 생각이 있습니다. 지금까지 해오던 방식으로도 잘만 굴러가는 서비스를 굳이 Amplify라는 도구를 학습해가며 쓸 이유는 없다고 생각하기 때문입니다. 물론 Amplify가 지금보다 더 발전한다면 모르지만요. :)
