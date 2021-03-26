## 브라우저에서 웹이 동작하는 과정

![브라우저와 웹서버 관계](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FNMHTD%2Fbtq0800IvPX%2FEacQrF8YL5ypxEXWm1M3l0%2Fimg.png)

웹을 실행하는 환경은 `브라우저`
웹을 제공하는 곳은 `웹 서버`

1.  사용자가 브라우저에서 URL(도메인 주소)를 입력
1. 브라우저는 웹 서버를 실행하고 있는 컴퓨터에게 요청
1. 웹 서버에서는 프론트엔드 개발자가 개발한 웹 페이지를 클라이언트(브라우저)에게 전달

---

### 웹 기본 3대장

![웹 기본 3대장](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Frohqf%2FbtqR6vvxV5F%2FZ1zHmw9jGeD3r2fkyWKQG0%2Fimg.jpg)

+ 브라우저는 기본적으로, `HTML` `CSS` `Javascript` 이 3가지 언어를 통해 웹을 보여줍니다.
+ 프론트엔트 개발자는 웹을 개발할 때, 기본적으로 이 3가지 언어(?)를 사용하게 됩니다.

간단하게 이 3가지를 정리하자면

+ `HTML` : **갖다놓고**
+ `CSS` : **꾸미고**
+ `Javascript` : **조작한다.**

**HTML, CSS는 `렌더링 엔진`을 통해 실행되며, Javascript는 `자바스크립트 엔진`을 통해 실행됩니다.**

![](https://www.grabbing.me/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F526aadc1-8ce6-48df-a07c-4174ab783cb5%2FUntitled.png?table=block&id=1c733467-b6c5-4ded-922a-3fc25eea90cb&width=1060&userId=&cache=v2)

1. 먼저 HTML을 통해, 기본적인 Element(텍스트, 링크 등)들을 적용한다.
2. CSS를 이용해, Element들에 디자인(색깔, 크기, 배치 등)을 씌운다.
3. **이미지**같은 다른 콘텐츠를 다운받는다.
4. Javascript가 적용된다.
	- 화면이 로드시, 정보를 API 서버에게 요청하거나
	- 버튼을 클릭하면, 버튼에 적용된 JS 코드가 실행되는 것
	

+ [브라우저 렌더링](https://janghanboram.github.io/2018/06/06/browser-rendering/) : **브라우저 화면에 웹을 그리는 전체적인 과정**
+ `렌더링` : **프로그래밍적으로 화면을 그리는 것**

---

### 서버 사이드 렌더링(SSR) 언어

![서버사이드 렌더링 언어](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcLM1zO%2Fbtq09ybwBb4%2FrOPtvYFtAAZDZgeTbOSijk%2Fimg.png)

**이들은 웹 서버에서 실행가능한 `서버 사이드 렌더링 가능 언어들 중 일부다.`

+ 웹 서버에서는 브라우저가 웹 요청(Request)을 했을 때, 웹(HTML, CSS, JS)을 넘겨주기 전에 코드를 미리 실행 할 수 있다.
+ 예를 들면, **미리 API 서버에서 정보를 받아와서 HTML, CSS 를 변경**할 수도 있다.
+ 이러한 방식들은 `SSR(Server Side Rendering`방식이라 한다.


