# <기술면접 정리>

## **객체지향 프로그래밍(Object Oriented Programming)**

객체 지향 프로그래밍은 기능을 제공하는 객체를 중심으로 프로그래밍하는 인간 중심적 프로그래밍 패러다임이다. OOP로 코드를 작성하는 경우 재사용성이 높아지며 디버깅과 유지보수에 용이하다. 하지만 객체 간의 정보 교환이 모두 메시지 교환을 통해 일어나므로 실행 시스템에 많은 overhead가 발생하지만 현재는 하드웨어의 발전으로 많은 부분 보완되었다. 그러나 OOP는 객체가 상태를 갖는다는 단점 때문에 변수가 존재하고 이 변수를 통해 객체가 예측할 수 없는 상태를 갖게 되어 애플리케이션 내부에서 버그가 발생한다. 이러한 단점 때문에 함수형 프로그래밍 패러다임이 등장하였다.

### **객체 지향적 설계 원칙**

1. SRP(Single Responsibility Principle) : 단일 책임 원칙
   클래스는 단 하나의 책임을 가져야 하며 클래스를 변경하는 이유는 단 하나의 이유이어야 한다.

2. OCP(Open-Closed Principle) : 개방-폐쇄 원칙
   확장에는 열려 있어야 하고 변경에는 닫혀 있어야 한다.

3. LSP(Liskov Substitution Principle) : 리스코프 치환 원칙
   상위 타입의 객체를 하위 타입의 객체로 치환해도 상위 타입을 사용하는 프로그램은 정상적으로 동작해야 한다.

4. ISP(Interface Segregation Principle) : 인터페이스 분리 원칙
   인터페이스는 그 인터페이스를 사용하는 클라이언트를 기준으로 분리해야 한다.

5. DIP(Dependency Inversion Principle) : 의존 역전 원칙
   고수준 모듈은 저수준 모듈의 구현에 의존해서는 안된다.

### **OOP의 특징**

1. 상속 : 클래스개념에서 하위 클래스가 상위 클래스의 메소드나 변수를 사용할 수 있는것

2. 다형성 : 같은 함수가 있어도 그 함수는 매개변수에 따라 다른 역할을 할 수 있다.

3. 캡술화 : 하나의 객체에 그 객체가 특정한 목정을 위해 필요한 변수나 메소드를 하나로 묶는 것. 이는 외부에서 데이터를 쉽게 접근할 수 없게 은닉해준다.

4. 추상화 : 공통적인 속성이나 기능을 묶어서 이름을 붙인다.

### **Overriding && Overloading**

1. Overriding은 부모 클래스에서 상속받은 자식 클래스에서 부모클래스의 메소드를 재정의해서 사용

2. Overloading은 같은 이름의 메소드를 사용하지만 각각 다른 용도로 사용하는것

## **함수형 프로그래밍(Functional Programming)**

함수형 프로그래밍이란 유지보수가 용이한 소프트웨어를 만들기 위해 함수를 사용하는 것을 의미한다.
이는 순수함수와 보조 함수의 조합을 통해 로직내에 존재하는 조건문과 반복문을 제거하고 복잡성을 해결하려는 프로그램 패러다임이다.

### **함수형 프로그래밍 특징**

1. 불변성
   함수형 프로그래밍은 외부에서 데이트를 수정하지 않는다. 이는 함수에 대한 입력 인수를 수정하지 않는것을 뜻하며 함수의 반환 값은 수행된 작업을 반영해야 부작용을 피할 수 있다.

2. 순수 함수
   함수형 프로그램밍은 순수 함수를 지향한다. 순수 함수란 결과값은 오지 입력 매개변수에 의해서만 좌우되는 반환 값 이외의 외부 영향이 없는 함수이다.

3. 일급 함수
   일급 함수는 독립적으로 취급이 가능한 함수다. 일급 함수는 다른 데이터 처럼 변수에 할당할 수 있다.

4. 고차 함수
   함수를 인수로 받거나 함수를 반환하는 함수를 고차 함수라고 한다.

## **REST API**

REST란 Representational State Transfer 의 약자로 월드 와이드 웹(WWW)와 같은 분산 하이퍼미디어 시스템을 위한 소프트웨어 아키텍처의 한 형식으로 자원을 정의하고 자원에 대한 주소를 지정하는 방법 전반에 대한 패턴이다. REST API는 크게 자원(URI), 행위(HTTP METHOD) , 표현으로 구성되어 있다.
(URI는 특정 리소스를 식별하는 통합 자원 식별자를 의미한다. URL은 네트워크 상에서 리소스가 어디 있는지 알려주기 위한 규약이다. )

### **REST의 특징**

1. Uniform (유니폼 인터페이스)
   Uniform Interface는 URI로 지정한 리소스에 대한 조작을 통일되고 한정적인 인터페이스로 수행하는 아키텍처 스타일을 뜻한다.

2. Stateless (무상태성)
   REST는 무상태성 성격을 갖는다. 즉, 작업을 위한 상태정보를 따로 저장하고 관리하지 않는다. 세션 정보나 쿠키정보를 별도로 저장하고 관리하지 않기 때문에 API 서버는 들어오는 요청만을 단순히 처리하면 된다. 이 때문에 서비스의 자유도가 높아지고 서버에서 불필요한 정보를 관리하지 않음으로써 구현이 단순해질 수 있다.

3. Cacheable (캐시 가능)
   REST의 가장 큰 특징 중 하나는 HTTP라는 기존 웹표준을 그대로 사용하기 때문에, 웹에서 사용하는 기존 인프라를 그대로 활용이 가능하다. 따라서 HTTP가 가진 캐싱 기능이 적용 가능하며, HTTP 프로토콜 표준에서 사용하는 Last-Modified태그나 E-Tag를 이용하면 캐싱 구현이 가능하다.

4. Self-descriptiveness (자체 표현 구조)
   REST API 메시지만 보고도 이를 쉽게 이해 할 수 있는 자체 표현 구조로 되어 있다.

5. Client - Server 구조
   REST 서버는 API 제공, 클라이언트는 사용자 인증이나 컨텍스트(세션, 로그인 정보)등을 직접 관리하는 구조로 각각의 역할이 확실히 구분되기 때문에 클라이언트와 서버에서 개발해야 할 내용이 명확해지고 서로간 의존성이 줄어들게 된다.

6. 계층형 구조
   REST 서버는 다중 계층으로 구성될 수 있으며 보안, 로드 밸런싱, 암호화 계층을 추가해 구조상의 유연성을 둘 수 있고 PROXY, 게이트웨이 같은 네트워크 기반의 중간매체를 사용할 수 있게 한다.

### **REST API 디자인 가이드**

1. URI는 정보의 자원을 표현해야 한다.

2. 자원에 대한 행위는 HTTP Method(GET, POST, PUT ,DELETE)로 표현한다.

## **TDD**

TDD란 Test-Driven Development의 약자로 매우 짧은 개발 사이클의 반복에 의존하는 소프트웨어 개발 프로세스이다. 개발자는 요구되는 기능에 대한 자동화된 테스트케이스를 작성하고 해당 테스트를 통과하는 간단한 코드를 작성하고 테스트를 통과하는 코드를 상황에 맞게 리팩토링하는 과정을 거친다. 즉, 테스트가 코드 작성을 주도하는 개발방식이다.

새로운 기능이 추가되는 경우 기존에 작동하던 기능이 작동하지 않는 경우가 발생 할 수 있으므로 TDD는 이러한 경우를 사전에 미리 방지 할 수 있다.

## **MVC**

MVC란 Model View Controller의 약자로 소프트웨어가 서비스하는 방식에 대한 패턴을 지칭한다.

1. Model
   DB에서 데이터를 가져오거나 데이터를 가지고 있을 수 있다. 이러한 데이터를 Controller에 전달하며 View와는 직접적으로 소통하자 않는다.

2. View
   유저가 보는 화면을 담당하며 Controller에게 전달받은 엑션이나 데이터를 화면에 그리는 역할을 한다.

3. Controller
   View에서 엑션과 이벤트에 대한 인풋 값을 전달받고 Model에전달하거나 전달하기 전 데이터를 가공한다. 또한 Model에게 받은 데이터를 가공하여 View에게 전달 할 수 있다.

### **JS 동작원리**

- https://asfirstalways.tistory.com/362
- https://sculove.github.io/post/javascriptflow/

### **HTTP의 GET과 POST 비교**

**GET**

- GET 방식은 요청하는 데이터가 HTTP Request Message의 Header 부분에 url 이 담겨서 전송된다. 때문에 url 상에 ? 뒤에 데이터가 붙어 request 를 보내게 되는 것이다. 이러한 방식은 url 이라는 공간에 담겨가기 때문에 전송할 수 있는 데이터의 크기가 제한적이다. 또 보안이 필요한 데이터에 대해서는 데이터가 그대로 url 에 노출되므로 GET방식은 적0절하지 않다.

**POST**

- POST 방식의 request 는 HTTP Request Message의 Body 부분에 데이터가 담겨서 전송된다. 때문에 바이너리 데이터를 요청하는 경우 POST 방식으로 보내야 하는 것처럼 데이터 크기가 GET 방식보다 크고 보안면에서 낫다.(하지만 보안적인 측면에서는 암호화를 하지 않는 이상 고만고만하다.)

- 그렇다면 이러한 특성을 이해한 뒤에는 어디에 적용되는지를 알아봐야 그 차이를 극명하게 이해할 수 있다. 우선 GET 은 가져오는 것이다. 서버에서 어떤 데이터를 가져와서 보여준다거나 하는 용도이지 서버의 값이나 상태 등을 변경하지 않는다. SELECT 적인 성향을 갖고 있다고 볼 수 있는 것이다. 반면에 POST 는 서버의 값이나 상태를 변경하기 위해서 또는 추가하기 위해서 사용된다.

- 부수적인 차이점을 좀 더 살펴보자면 GET 방식의 요청은 브라우저에서 Caching 할 수 있다. 때문에 POST 방식으로 요청해야 할 것을 보내는 데이터의 크기가 작고 보안적인 문제가 없다는 이유로 GET 방식으로 요청한다면 기존에 caching 되었던 데이터가 응답될 가능성이 존재한다. 때문에 목적에 맞는 기술을 사용해야 하는 것이다.

### **HTTP와 HTTPS**

**HTTP란**

- 클라이언트와 서버의 데이터전송 프로토콜(규칙)
- HTTP는 클라이언트의 요청을 받고 서버가 응답을하면 그 연결을 끊어버려서 서버는 매 요청시 사용자가 누군지 확인해야하는 단점이있다. 이를 보완하기 위해 쿠키와 웹스토리지를 사용한다.

**HTTPS**

- HTTPS는 SSL 의 껍질을 덮어쓴 HTTP 라고 할 수 있다. 즉, HTTPS 는 새로운 애플리케이션 계층의 프로토콜이 아니라는 것이다. HTTP 통신하는 소켓 부분을 SSL(Secure Socket Layer) or TLS(Transport Layer Security)라는 프로토콜로 대체하는 것 뿐이다. HTTP 는 원래 TCP 와 직접 통신했지만, HTTPS 에서 HTTP 는 SSL 과 통신하고 SSL 이 TCP 와 통신 하게 된다. SSL 을 사용한 HTTPS 는 암호화와 증명서, 안전성 보호를 이용할 수 있게 된다.

HTTPS 의 SSL 에서는 공통키 암호화 방식과 공개키 암호화 방식을 혼합한 하이브리드 암호 시스템을 사용한다. 공통키를 공개키 암호화 방식으로 교환한 다음에 다음부터의 통신은 공통키 암호를 사용하는 방식이다.

### **Cookie & Session**

**저장 위치**

- 쿠키 : 클라이언트의 웹 브라우저가 지정하는 메모리 or 하드디스크
- 세션 : 서버의 메모리에 저장

**만료 시점**

- 쿠키 : 저장할 때 expires 속성을 정의해 무효화시키면 삭제될 날짜 정할 수 있음
- 세션 : 클라이언트가 로그아웃하거나, 설정 시간동안 반응이 없으면 무효화 되기 때문에 정확한 시점 알 수 없음

**리소스**

- 쿠키 : 클라이언트에 저장되고 클라이언트의 메모리를 사용하기 때문에 서버 자원 사용하지 않음
- 세션 : 세션은 서버에 저장되고, 서버 메모리로 로딩 되기 때문에 세션이 생길 때마다 리소스를 차지함

**용량 제한**

- 쿠키 : 클라이언트도 모르게 접속되는 사이트에 의하여 설정될 수 있기 때문에 쿠키로 인해 문제가 발생하는 걸 막고자 한 도메인당 20개, 하나의 쿠키 당 4KB로 제한해 둠
- 세션 : 클라이언트가 접속하면 서버에 의해 생성되므로 개수나 용량 제한 없음

**캐시**

- 쿠키와 같이 클라이언트에 저장되는 파일이지만 이미지 같이 재사용성이 높거나 용량이 큰 데이터를 저장하기 위한 목적

**웹스토리지**

- 클라이언트에 데이터를 저장하지만 저장한 데이터는 서버로 넘어가지 않는다.
- key / value형태로 저장

**EX**

- 자동 로그인 -> 로컬스토리지

- 입력 폼 정보 -> 세션스토리지

- 비로그인 장바구니 -> 세션스토리지

- 다시 보지 않음 팝업 창 -> 쿠키

## **CSS in CSS / CSS in JS**

- https://www.samsungsds.com/kr/insights/web_component.html

## **데이터 바인딩**

- client와 server의 메모리에 있는 데이터를 일치시키는것

1. 양방향 데이터 바인딩

- 코드량이 크게 줄어들고 유지보수가 쉬운 장점이 있지만 DOM 객체 전체를 렌더링해줘야 하므로 성능이 감소된다.
- MVC 패턴에서 컨트롤러와 뷰 양쪽의 데이터를 일치시키는 것

2. 단방향 데이터 바인딩

- 성능저하 없이 DOM객체 갱신이 가능하며 데이터 추척이 쉽다
- 데이터의 변화를 감지하고 화면을 업데이트 하는 코드를 매번 작성해야 하는 단점이 있다.

## **HTTP Header**

- 헤더는 body 및 res/req에 대한 정보를 포함한다.

1. 일반헤더

- body컨테츠와 관련이 없고 res/req 생성된 날짜 및 시간등 일반적인 정보가 포함된다.

2. 요청 / 응답 헤더

- 요청항 URL , 메소드 등 정보가 포함된다.

3. 엔티티 헤더

- body 데이터를 해설할 수 있는 정보가 포함된다.

## **HTTMP Body**

- 메세지 본문을 통해 데이터를 전달하며 메세지 본문을 payload라 한다.

## **PWA란?**

- PWA는 모바일 웹 에서도 네이티브앱과 같은 기능을 제공하는 기술 (트위터가 사용)
- ex ) 홈화면 설치 / 푸시 알림 등등
- 일발 웹과 다르게 프리캐시 기능이 있어 페이지를 보고있는 동안 다음 페이지를 로드한다. 또한 백그라운데에서 업데이트하기 때문에 사용자는 다시 로드할 필요가 없다.
- 앱스토어에 출시하지 않아도되며 일반적인 웹기술로 구현할 수 있다. 또한 오프라인에서도 작동한다.
- SEO(검색엔진 최적화)를 위해 SSR를 적용하는것이 좋을거라 생각된다.

## **인증 / 인가**

- 인증은 로그인을 요청하여 사용자를 확인하는 것
- 인가는 로그인된 (인증된) 유저가 서비스를 사용할 수 있게 허가해주는 것

## **CORS**

- 교차 출처 리소스 공유(Cross-Origin Resource Sharing)란 HTTP헤더를 사용하여 한 출처에서 실행중인 애플리케이션이 다른 출처의 선택한 리소스에 접근할 수 있도록 권한을 부여하는 체제이다.
- Origin은 scheme(protocol => HTTPS) / host(domain) / port로 구성된다.
- 브라우저는 보안상의 이유로 교차 출처 HTTP요청을 제한하기 떄문에 CORS에러가 발생한다.

**CORS 동작흐름**

- 브라우저는 req Header의 Origin 필드에 요청을 보내는 출처를 담아서 전송한다.
- 서버는 res Header에 Access-Control-Allow-Origin이라는 값에 접근을 허용해줌을 브라우저로 보내고 브라우저는 Origin과 서버가 보내준 Access-Control-Allow-Origin을 비교하여 판단한다.

**CORS오류 해결방법**

1. 서버측 응답에서 접근권한 헤더를 추가

```
app.use((req, res, next) => {
  res.header("Access-Control-Allow-Origin", "*"); // 모든 도메인
  res.header("Access-Control-Allow-Origin", "https://example.com"); // 특정 도메인
});
```

2. cors모듈 사용

```
const cors = require("cors");
const app = express();

app.use(cors());
// 특정 도메인만 허용시
const options = {
  origin: "http://example.com", // 접근 권한을 부여하는 도메인
  credentials: true, // 응답 헤더에 Access-Control-Allow-Credentials 추가
  optionsSuccessStatus: 200, // 응답 상태 200으로 설정
};
```

## **JWT**

- 인증에 필요한 정보를 Token에 담아 암호화시켜 사용

1. Header

- 토큰의 타입 / 어떤 알고리즘이 사용되었는지 지정

2. Payload

- 사용자 / 토큰에 대한 정보를 key-value형태로 저장
- 쉽게 decoded될 수 있으므로 민감한 정보는 제외한다.

3. Signature

- 메시지가 중간에 변경되지 않고 전송받은 JWT가 신뢰할 수 있다는것을 나타낸다.

## **바벨**

- 바벨은 새로운 문법이나 TS JSX와 같은 문법들을 모든 브라우저에서 동작할 수 있도록 변환해준다. 즉 하위버전의 JS언어로 변환시켜준다.

## **웹팩**

- 웹팩은 모듈 번들러이다. / 번들러란 필요한 의존성을 추적하여 해당하는 의존성들을 그룹핑 해주는 도구이다.
- 번들러를 사용하면 여러 개의 파일을 하나로 묶어주기 때문에 네트워크 접속의 부담을 줄여 더 빠른 서비스를 제공할 수 있다.
- 웹팩은 다수의 JS / CSS등의 파일을 하나의 JS파일로 만들어준다.

## **CI/CD**

1. CI

- Continuous Integration(지속적인 통합)은 어플리케이션의 새로운 코드 변경 사항이 정기적으로 빋드 및 테스트되어 공유 레포지토리에 통합되는 것

2. CD

- Continuous Depolyment(지속적인 배포) / Continuous Delivery(지속적인 서비스)의 축약어
- Continuous Delivery는 공유 레포지토리로 자동으로 Release 하는 것이고
- Continuous Depolymentsms production레벨까지 자동으로 deploy하는 것
