# What is Full Cycle and FCD(Full Cycle Developer)?

### Full Stack은 들어봤는데, Full Cycle?

벌써 1년도 전에 넷플릭스의 개발 문화 중 하나로 알려진 [넷플릭스의 풀사이클 개발자에 대한 글](https://medium.com/netflix-techblog/full-cycle-developers-at-netflix-a08c31f83249)이 미디엄에 널리 퍼졌었습니다. 그 개념은 스타트업의 상상의 동물 중 하나인 풀스택 개발자와 유사합니다. 흔히 말하는 풀스택 개발자는 애플리케이션 개발에 필요한 모든 기술을 다루는 엔지니어를 뜻하는데, 흔히 다음 키워드를 실무에서 적용시킬 수 있는 엔지니어를 말하곤 합니다.

* 프론트엔드, 백엔드
* 데이터베이스
* 데브옵스
* 아키텍트

풀스택과 풀사이클 개발자의 차이는 [Full Stack vs Full Cycle developer - Elton Minetto](https://dev.to/eminetto/full-stack-vs-full-cycle-developer-50hf)를 찾아보면 어느정도 설득력있게 말하지만, [6 Essential Tips on How to Become a Full Stack Developer](https://hackernoon.com/6-essential-tips-on-how-to-become-a-full-stack-developer-1d10965aaead)을 통해 알 수 있는 것처럼, 사실상 그 둘을 구분하는 일은 자장면이나 짜장면이냐를 이야기하는 것과 같이 애매모호하기 때문에 이 글에서는 굳이 구분하지 않고 둘을 혼용해 사용하도록 하겠습니다. 그냥 둘 다 개발 전반을 담당하는 엔지니어인 건 변함없으니까요!

다시 본론으로 돌아와서 풀사이클 개발에 대해 알아보면, 넷플릭스의 정의는 하나의 문제를 해결하기 위한 해결 과정을 하나의 사이클로 생각하고, 개발팀은 그 문제에 대한 설계, 개발, 테스트, 배포, 운영 전반을 담당해 처리한다고 이야기한다고 합니다(물론 그 조건은 with amazing developer productivity tools이지만 말이죠).

> […] we arrived at a model where a development team, equipped with amazing developer productivity tools, is responsible for the full software life cycle: design, development, test, deploy, operate, and support.

물론 이 주제는 의견이 분분할 수 있는 주제이기 때문에, 오늘 이 자료에서는 넷플릭스가 이야기한 풀사이클 개발이 무엇인지에 대한 감을 잡고, '많고 많은 개발 문화 중 하나'라고 생각해주시면 감사하겠습니다.

### Full Stack이 정말 존재하긴 하는 거야?

만약 이 글을 읽는 분들 중 스타트업에 계신 분이 있다면, 대부분 의도하든 의도하지 않든 풀스택으로 업무를 진행하고 계실 겁니다. 물론 스타트업과 어느정도 규모가 있는 회사 각각에서 필요로하는 풀스택 개발자의 역량은 다르지만, 서두에 언급했던 것처럼 기능 혹은 운영을 포함한 개발 프로세스 전반을 담당하는 엔지니어임은 틀림없습니다.

국내에서도 처음에는 뜬구름이라고 불렸던 풀스택 개발은 그 시작이 실리콘밸리인 것처럼 링크드인, 페이스북처럼 실리콘밸리의 유명한 회사들이 채용하는 직군[1](https://www.facebook.com/careers/jobs/1662909867342164/)[2](https://www.linkedin.com/jobs/search/?f_C=1337%2C2587638%2C39939%2C290903%2C9202023%2C2561065&keywords=Full-stack%20Developer&location=%EC%A0%84%EC%84%B8%EA%B3%84&locationId=OTHERS.worldwide)의 필요 역량 중 하나로 언급되기도 하고, 국내의 NHN, 샌드버드[1](https://recruit.nhn.com/ent/recruitings/20001244)[2](https://sendbird.com/careers/4319814002)에서도 따로 채용하는 걸 보면 이제는 시장이 필요로 하는 하나의 직군으로 자리잡고 있는 듯 합니다.

### 그렇다면, 과연 주니어가 Full Stack을 담당하는 건 어불성설일까?

제가 만나봤던 시니어 분들 중 일부 분들은 풀스택을 하나의 허세로 생각하시기도 합니다. 아니면 웹으로 치자면 프론트엔드, 백엔드 둘 중 하나도 제대로 모르면서 어떻게 풀스택으로 일할 수 있느냐며 프론트엔드와 백엔드 중 한 분야에서 어느정도 실력을 쌓고 안목을 넓히다보면 자연스럽게 풀스택이 된다고 말하시기도 합니다.

물론 어느정도 맞는 말이고, 충분히 동의할 수 있습니다. 하지만, 급변하는 시장의 필요 혹은 리모트 근무를 추구하는 문화의 확대 등에 따라 변하고 있는 최근 개발 프로세스의 흐름을 보면, 한 명의 엔지니어가 풀스택으로 개발하는 것은 모든 팀은 아니더라도 혁신을 추구하며 안정성보다는 빠른 변화를 추구하는 팀에서는 필수적으로 갖춰야 할 능력이라고 이야기할 수도 있을 것입니다.

### 그렇다고 풀스택 개발자가 만사형통은 아닙니다!

이 글을 읽는 비개발 직군 혹은 CTO 분들께서 풀스택 개발자를 채용하거나 풀스택으로 개발하는 조직을 구하려 하신다면, 가장 먼저 물리적인 한계를 고려해야 한다는 것을 아셔야 합니다(물론 개발 직군이신 분들만 관심있으시겠지만요).

풀스택 개발은 설계부터 프론트엔드와 백엔드, 인프라를 비롯한 운영 전반까지를 하나의 팀 혹은 한 명의 엔지니어가 담당하기 때문입니다. 가령 하나의 토스트를 만들 때 오버해서 `빵(1kg) + 채소(1kg) + 햄(1kg) = 토스트(3kg)`으로 만드는 게 아니라 `빵(0.3kg) + 채소(0.3kg) + 햄(0.4kg) = 토스트(1kg)`으로 만들어야 하는 것처럼 풀스택 엔지니어의 업무량도 물리적인 인적 자원의 한계를 고려해 생각해야 합니다(풀스택 한 명 있다고 1달만에 앱이 배포되는 건 아니란 말입니다! 우리의 개발자를 살려주세요...).

그렇다면 이제 풀스택, 그러니까 풀사이클 개발에 대한 제 개인의 주관이 포함된 대략적인 설명을 끝내고 [다음 자료](chapter3.md)로 이동하시길 바라겠습니다.

#### 참고 자료

[2018 05 넷플릭스 개발 문화 - Full Cycle Developers at Netflix — Operate What You Build(영문)](https://medium.com/netflix-techblog/full-cycle-developers-at-netflix-a08c31f83249)
[2018 05 넷플릭스 개발 문화 - Full Cycle Developers at Netflix — Operate What You Build(한글 번역)](https://brunch.co.kr/@imagineer/293)
