![https://s3.ap-northeast-2.amazonaws.com/kblockr/kblock+01.png
](https://s3.ap-northeast-2.amazonaws.com/kblockr/kblock+01.png
)
## Kblock 공식 리서치팀, 케블리
-------------
</br></br>
<b>안녕하세요 케블리 입니다.</b> 케블리는 '전세계의 블록체인 비즈니스를 함께 찾고 공부해 나눈다’는 KBlock의 목표에서 ‘나눈다’를 본격적으로 실천합니다.
</br>

-----------------------------
</br></br>

## #17 DelegateCall.com

### 첫인상

DelegateCall.com은 블록체인 기반의 블록체인 Q&A 웹사이트 입니다. 

![DY0VqBJU0AAQW71.jpg](https://steemitimages.com/DQmVeZK6JpQRtdUdfbsHb8i4ShWuHwyFwxVjJKHDhjVxwaZ/DY0VqBJU0AAQW71.jpg)

이 웹사이트를 이용하는 방법은 우리가 그 동안 알고 있던 Q&A 웹사이트를 이용하는 방법과 완전히 같습니다. 단, 활동에 따른 보상을 이더리움 토큰(이름은 델리게이트콜 토큰 입니다)으로 받는다는 점이 일반 웹사이트와 다릅니다.

![스크린샷 2018-03-24 오후 2.57.33.png](https://steemitimages.com/DQmVznuHJyS1wgvHgbWpUqPiwf1Xpey5NAQ2QGL4cKJaayH/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202018-03-24%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%202.57.33.png)

DelegateCall.com은 룸 네트워크(Loom Network) 기반으로 어떤 DApp을 만들 수 있는지 보여주기 위해 룸 네트워크 팀이 직접 구현한 서비스입니다. 

### 룸 네트워크(Loom Network)

룸 네트워크는 **대규모** 온라인 게임과 소셜 애플리케이션을 위한 블록체인 플랫폼을 표방하고 있습니다. 아시다시피 이더리움은 아직 대규모 서비스를 하기에는 한계를 보여주고 있습니다. 그래서 이더리움 자체도 확장성 확보를 위해 노력 중이고, 이더리움의 한계를 극복하기 위한 다양한 프로젝트가 시도되고 있습니다. 룸 네트워크의 핵심 아이디어는 DApp 마다 사이드 체인을 갖도록 함으로써 이더리움의 확장성 문제를 해결하는것 입니다. 룸 네트워크는 DApp별 사이드 체인을 DAppChain이라고 부릅니다. 

룸 네트워크는 DApp에서 발생하는 모든 액션이 모두 똑같이 최고의 보안 수준을 필요로 하지 않는다는 점에 주목했다고 합니다. 트윗 같은 게시물에도 금융 트랜잭션과 같은 수준의 보안을 적용함으로써, 이더리움 사용자들은 최고 수준의 보안이 필요하지 않을 때에도 DApp의 함수를 실행하기 위해 더 많은 비용을 지불하고 있다고 지적합니다. DAppChain에서 발생하는 모든 트랜잭션은 해당 DApp에 한정하여 발생하므로, 특정한 타입의 트랜잭션에 최적화된 합의 알고리즘을 체인에 적용할 수 있습니다. DApp 체인은 메인 체인의 규칙을 따를 수도 있어서, 최고 수준의 보안이 필요한 문제에 대해서는 메인 체인에 의존하면서도 매우 빠른 속도나 많은 연산이 필요한 애플리케이션에 최적화 될 수 있다고 합니다. 

예를 들어, DelegateCall은 DPOS(Delegated Proof of Stake, 위임된 지분증명)를 사용합니다. DPOS는 이더리움이 사용하는 POS 합의 알고리즘의 변형입니다. 블록을 업데이트하기 위해 모든 사용자가 합의를 해야하는 POS와 달리, DPOS는 권한을 위임받은 사용자들만 합의를 하면 됩니다. 따라서, 처리속도가 훨씬 빠릅니다. Steemit.com으로 유명한 Steem 블록체인이 DPOS를 사용하고 있는데, Steem은 21명의 사용자가 권한을 위임받아 합의를 합니다. DelegateCall의 DPOS는 아직 구체적으로 공개되진 않았습니다. 

![](https://loomx.io/images/DAppchain-160e4c60.png)

### DelegateCall.com 다시보기

DelegateCall.com은 사용자로서의 느낌은 일반 웹사이트와 같지만 내부 구조는 일반 웹사이트와 완전히 다릅니다. 

![](https://cdn-images-1.medium.com/max/800/1*gHyY25cIMI_mkoFm6nlChA.png)

위의 그림은 조금 복잡해보이지만 간단히 요약하면, 일반 웹사이트처럼 데이터를 데이터베이스에 저장하지 않고, 블록체인에 저장한다는 것입니다. (그림에서 맨 위에 있는 client가 loom.js를 이용해서 DelegateCall DappChain에 연결되는 것에 주목하세요.) 그러면 Worker가 블록체인의 데이터를 가져다가 (전통적인) SQL 데이터베이스와 검색엔진에 업데이트하고, 웹 애플리케이션은 이 데이터베이스와 검색엔진에서 데이터를 가져와서 사용자에게 보여줍니다.

보상을 지급한다는 것 이외에는 일반 웹사이트와 똑같이 생겨서 간과할 수도 있지만, 블록체인에 기반한 애플리케이션이기 때문에 블록체인의 특징을 그대로 갖고 있습니다. 즉, ‘커뮤니티에 의해 운영되고, 누구도 검열할 수 없는' 특징을 갖습니다. 룸 네트워크는 DAppChain에서 운영되는 DApp의 데이터는 공개되고 공유될 수 있으며, 민주적이라고 이야기 합니다. DApp을 지원하고 개발과정에 투표할 권리를 얻고 싶은 유저는 노드를 운영하여 권리를 획득할 수 있습니다. 노드를 운영하는 사용자는 DAppChain의 모든 데이터의 복사본을 갖게 됩니다. 개발자들은 사용자들이 원치 않는 업데이트를 할 수 있지만 이 경우 사용자들이 거부하거나 의견을 전달 할 수 있는데, 이러한 것들이 거부되면 직접 다른 애플리케이션을 만들 수도 있습니다. 개발자와 동일 데이터를 가지고 있기 때문에 가능한일입니다.

### 탈중앙 마인드

저는 계속해서 블록체인으로 무얼 할 수 있지?를 궁금해 해왔고, 케블리에서 활동하는 이유도  그 궁금증을 해결하는 것입니다. ‘블록체인이 인터넷의 미래다'라는 식의 이야기를 들을 때마다 ‘블록 생성에 저렇게 오랜 시간이 걸리는데, 과연 현재 인터넷의 많은 부분을 대체할 수 있을까?’라는 생각을 해왔습니다. 이번에 DelegateCall.com을 보고나니 현재 인터넷 상에 구현된 왠만한 애플리케이션은 다 블록체인 기반 애플리케이션으로 만들 수도 있겠구나라는 생각이 드네요. 

기존 웹 애플리케이션과 동일한 사용성을 제공하면서도, 이더리움과 호환되는 토큰을 제공할 수 있다? 참 매력적입니다. 하지만, 민주적이고, 커뮤니티에 의해 운영된다는 부분이 기존의 비즈니스에 익숙한 사람들로 하여금 블록체인 활용을 주저하게 만들 수도 있을 것 같습니다. 내 노력의 결과가 오로지 내것이 아닌 셈이기 때문이죠. 자신의 사업을 시작하는 사람은 대게 자기 주도적으로 무언가를 하고 싶어 합니다. 또한 ‘내 것’에 대한 소유욕이 강하죠. 하지만 블록체인을 인프라로 삼으면 데이터는 모두의 것이 되고, 계속해서 커뮤니티를 설득해가며 일을 진행해야 합니다. 일을 해보신 분들은 아시겠지만 여러 사람을 설득해가며 일을 하는 것은 무척 피곤한 일입니다. 어쩌면 블록체인을 기반으로 제품을 만든다는 것은 기존의 비즈니스 마인드와는 다른 ‘탈중앙적' 마인드를 가진 사람이어야 제대로 기획하고 운영할 수 있는건 아닐까라는 생각을 하게 한 사례였습니다.

### 참고자료

- [룸 네트워크 홈페이지](https://loomx.io/)
- [DelegateCall.com](https://delegatecall.com)
- [백만 명이 사용할 수 있는 이더리움 DApp: 애플리케이션별 사이드체인에 대한 소개](https://medium.com/loom-network-korean/%EB%B0%B1%EB%A7%8C-%EB%AA%85%EC%9D%B4-%EC%82%AC%EC%9A%A9%ED%95%A0-%EC%88%98-%EC%9E%88%EB%8A%94-%EC%9D%B4%EB%8D%94%EB%A6%AC%EC%9B%80-dapp-%EC%95%A0%ED%94%8C%EB%A6%AC%EC%BC%80%EC%9D%B4%EC%85%98%EB%B3%84-%EC%82%AC%EC%9D%B4%EB%93%9C%EC%B2%B4%EC%9D%B8%EC%97%90-%EB%8C%80%ED%95%9C-%EC%86%8C%EA%B0%9C-ed5d35b56d28)
- [DAppChains: 사이드체인을 통한 이더리움 DApp 확장](https://medium.com/loom-network-korean/dappchains-%EC%82%AC%EC%9D%B4%EB%93%9C%EC%B2%B4%EC%9D%B8%EC%9D%84-%ED%86%B5%ED%95%9C-%EC%9D%B4%EB%8D%94%EB%A6%AC%EC%9B%80-dapp-%ED%99%95%EC%9E%A5-f35f82b97aaa)
- [DelegateCall.com: 룸 네트워크의 첫 번째 DAppChain](https://medium.com/loom-network-korean/delegatecall-com-%EB%A3%B8-%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC%EC%9D%98-%EC%B2%AB-%EB%B2%88%EC%A7%B8-dappchain-f7ebb3ebcf7a)
- [Loom Network 출시! DAppChain을 통해 확장성 있는 이더리움 DApp이 곧 만들어집니다.](https://medium.com/loom-network-korean/loom-network-%EC%B6%9C%EC%8B%9C-b2aa56673202)

<br />
![이현석](https://steemitimages.com/DQmWFDvi6jv388SqzabT2pn2iiXjQ2mF7q2mLthxuquvyYi/%EC%9D%B4%ED%98%84%EC%84%9D.png)