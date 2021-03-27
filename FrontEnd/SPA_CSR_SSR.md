## SPA 와 CSR & SSR

### SPA(Single Page Application)

![](https://linked2ev.github.io/assets/img/devlog/201808/2018-08-01-SPA-step3.png)

`SPA` 는 말 그대로, 한개의 페이지를 가진 애플리케이션

> 왜 SPA로 개발하느냐 ?

+ 사용자 친화적
+ 초기 렌더링 후, **데이터만 받아오기 때문에**, 상대적으로, **서버 요청이 적음(서버 부담이 적음)**
+ [Virtual Dom](https://ko.reactjs.org/docs/faq-internals.html)
+ FE(프론트엔드)와 BE(백엔드)의 분리로 개발업무 분업화 및 협업이 용이
+ 개발이 상대적으로 효율적

기본적으로 **SPA**는 **클라이언트 사이트 렌더링(CSR)**이지만, 그렇다고 SPA === CSR은 아닙니다.

---

### CSR & SSR

**웹이 웹 서버와 통신해서 웹을 다운받는 방식은 크게 2가지**

+ `CSR(Client Side Rendering)`
+ `SSR(Server Side Rendering)`

이렇게 2가지 방식이 존재합니다.

**CSR**

![CSR 초기 데이터 로드전](https://miro.medium.com/max/1400/1*c955FMt4om-cyNU9d11OiQ.png)

+ 초기 웹 서버 요청 시, 데이터가 없는 빈 문서를 반환

![CSR 데이터 로드후](https://miro.medium.com/max/1400/1*nmfJo2FUGSF9aL45JwG-Lg.png)

+ HTML 및 static(정적)파일들이 로드 되면서 데이가 있다면, 데이터 또한 서버에 요청하고 그것이 화면에 나타나는 방식이다.

**브라우저가 서버에 HTML 및 static 파일들만 받아 첫 로딩이 완료되면, 사용자의 상호작용에 따라, Javascript를 통해 동적으로 Rendering한다. 필요에 따라 데이터를 서버에 요청해서 받아와 Rendering 한다.**

+ 장점

	- 첫 로딩에 HTML 및 Static 파일들만 다 받으면, 동적으로 빠르게 렌더링하기 때문에, 사용자 UX가 뛰어나다.
	- 서버에 요청하는 횟수가 훨씬 적어, 서버 부담이 덜하다.
	
+ 단점
	
	- 초기에, 모든 HTML 및 Static 파일이 로드될 때까지 기다려야 한다.
	- 이러한 단점때문에, [SEO(검색엔진 최적화)](https://ko.wikipedia.org/wiki/%EA%B2%80%EC%83%89_%EC%97%94%EC%A7%84_%EC%B5%9C%EC%A0%81%ED%99%94)에 문제가 발생할 수 있다.

![](https://d2.naver.com/content/images/2020/06/csr.png)

**SSR**

![SSR 방식](https://miro.medium.com/max/1400/1*fuDcEQEaNQXEg4S78n-lUQ.png)

**완전히 만들어진 HTML 파일을 받아오고 Rendering 한다.**

+ 장점

	- 초기 로딩 속도가 빠르기 때문에 사용자가 컨텐츠를 빨리 볼 수 있다.
	
	- 모든 검색엔진에 대한 SEO(검색엔진 최적화)가 가능하다.
	
+ 단점

	- 매번 페이지를 요청할 때마다 **새로고침** 되기 때문에 사용자 UX가 다소 떨어진다.
	- 서버에 매번 요청을 하기 때문에 트래픽, 서버 부하가 커진다.
	
![](https://d2.naver.com/content/images/2020/06/ssr.png)

---

### 마무리

**대부분 CSR 렌더링 방식을 사용 시, SPA 형태로 웹을 만든다.**

+ 대표적으로 `React` `Vue` `Angular` 프레임워크가 CSR 렌더링 방식에 SPA 형태로 제공한다.

**그러나, React, Vue에서도 SSR 렌더링 방식이 가능하다.**
**SSR 전용 React, Vue 프레임워크로 React에 경우`NextJs` Vue에 경우는 `NuxtJs` 가 있다. 
클라이언트가 빠르게 웹에 접근할 수 있도록 SSR을 적용하는 기업들이 늘어나는 추세이다.**

