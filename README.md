# 💪 HTML, CSS 기초 공부

## HTML

### 1. 강조(strong, em)

> 문장을 작성하다가 강조 효과를 넣고 싶을 때는 strong, em을 사용한다.
>
> - strong  
>   strong은 글씨가 두꺼워 지는 효과를 가진다.
> - em  
>   em은 글씨를 기울어지게 하는 효과를 가진다.

```html
<p lang="en">
  hello!dklafn;sdfns;fn;sdkfnsfn;asf <br />
  <strong>굵게 쓰고싶다!</strong> aklsn;fkaensf;snfa;es <br />
  <em>기울여 쓰고싶다!</em>
  asf;ns;fknas;fsdfdsfa
</p>
```

강조하고 싶은 부분을 태그로 감싸주면 된다!

### 2. 링크(a)

> 흔히 알고있는 하이퍼링크 처럼 특정 웹 주소에 연결해주는 기능을 한다.  
>  태그 내에 attr을 적절하게 사용하면 다양한 기능을 구현할 수 있다.  
>  구현 가능한 기능은 아래와 같다.
>
> - 웹 url 입력
> - 상대 경로 입력
> - 메일 작성
> - 전화 걸기

```html
<a href="http://www.naver.com">웹 url 링크.. hypertext reference == href</a>
<br />
<a href="http://www.naver.com" target="_blank">이건 새로운 탭에서 열어준다.</a>
<br />
<a href="">다른 파일의 상대 경로도 입력 가능</a> <br />
<a href="#hello">id를 활용해서 페이지 내 이동 가능</a> <br />
<a href="mailto:pky00823@naver.com">링크된 이메일로 메일 쓰기</a> <br />
<a href="tel:01012345678">모바일에서 사용시...전화 걸기 가능</a> <br />
<a href="http://www.naver.com" target="_blank">
  <p>
    이 글을 누르면 네이버로 이동하게 될거야!! 이런 식으로 표현 할 수도 있어~
  </p>
</a>
```

첫 째, 단순하게 url을 적어서 해당 웹 페이지로 이동하는 것이다.  
여기서 **target: \_blank**를 사용하면 새로운 탭에서 웹 페이지가 열리도록 만들 수 있다.

둘 째, 상대 경로를 입력하는 것이다. 만약, 여러개의 HTML 파일을 만들게 된다면 그 파일의 위치를 입력함으로서 그 페이지로 이동할 수 있는 것이다.

셋 째, **mailto:** 를 사용하여 링크되어있는 이메일 주소로 메일 쓰기가 가능하다.

넷 째, **tel:** 을 사용하여 링크되어있는 휴대전화 번호로 전화가 가능하다. 이는 휴대전화에서 웹 페이지를 사용할 때 매우 유용하게 쓰일 기능이다.

그 외, p 태그 등을 활용한 문장이나 이미지 카드 등에도 a 태그로 감싸주면 링크를 연결할 수 있다.

### 3. 이미지(img)

> 이미지는 **src**(source)에직접 이미지 url을 입력해서 불러올 수도 있고, 상대 경로를 지정해서 파일에 저장된 이미지를 불러올 수도 있다.  
>  **alt**(alternative)는 이미지가 로딩되지 못하는 상황에 그 자리를 대체하도록 하는 텍스트이다. 이는 장애가 있으신 분들을 위해 웹을 읽어주는 기능이 작동할 때 이미지 대신 읽히는 부분이기도 하다.

```html
<img
  src="https://newsroom-prd-data.s3.ap-northeast-2.amazonaws.com/wp-content/uploads/2018/08/b_01.png"
  alt="여행 이미지"
/>
<img src="./images/b_01.png" alt="" />
```

### 4. 리스트(ul, ol, li)

> 리스트는 순서가 없다면 **ul**(unordered list)를 사용한다.  
>  순서가 있다면 **ol**(ordered list)를 사용한다.  
>  ul과 ol은 직계 자식요소로 **li**(list item)만을 가진다. 즉, 다른 태그는 자식 요소로 사용할 수 없다는 뜻이다.  
>  만약, 다른 태그를 사용하고 싶다면 li 태그로 감싸서 사용해야한다.

```html
<ul>
  <li>unordered list == ul</li>
  <li>list item == li</li>
  <li>ul 직계 자식요소는 li만 가능하다. li 안에 다른 태그를 넣는 것은 가능</li>
  <li><a href="http://naver.com" target="_blank">네이버</a></li>
  <li>순서가 따로 정해져 있지 않다</li>
</ul>
<h2>급상승 검색어</h2>
<ol>
  <li>orderd list == ol</li>
  <li>순서가 있어야 하는 리스트에 사용</li>
  <li>주니어 개발자</li>
  <li><a href="http://naver.com">네이버</a></li>
</ol>
```

**ol**의 경우 기본적으로 숫자가 붙어서 순서를 표시해준다.  
리스트 맨 앞에 표시되는 모양은 태그에 attr을 추가로 입력해서 바꿀 수도 있고, CSS를 사용해서 바꿀 수도 있다.

### 5. 정의 리스트(dl, dt, dd, dfn)

> 백과사전 처럼 용어의 뜻을 표시할 때 쓰는 태그이다.  
> 혹은 key & value 로 정보를 제공할 때도 쓰인다.
>
> dl == description list  
> dt == description term  
> dd == description data  
> dfn == definition

```html
<dl>
  <dt>
    <dfn> 박기영 </dfn>
  </dt>
  <dt>Pak ki young</dt>
  <dd>박기영은 하루빨리 프론트엔드 개발자가 되고싶다.</dd>
  <dd><a href="http://www.naver.com">gg</a></dd>
  <dt>프론트 엔드</dt>
  <dd>박기영은 프론트엔드 개발자가 되고싶어!</dd>
  <dd>백엔드와 연결이 되는 직업!</dd>
  <div>
    <dt>이렇게도 가능하지</dt>
    <dd>박기영은 프론트엔드 개발자가 되고싶어!</dd>
    <dd>백엔드와 연결이 되는 직업!</dd>
  </div>
</dl>
```

4번에서 다룬 리스트와 마찬가지로 **dl**의 직계 자식요소로는 **dt, dd, dfn, div**만 가능하다.  
따라서 다른 태그를 사용하고 싶다면 직계 자식요소 태그들로 감싸서 사용해야한다.  
참고로, **dfn** 태그는 **em** 태그의 효과처럼 텍스트가 기울어진 형태로 표시된다.

### 6. 인용문(blockquote, q)

> blockquote의 경우 문단이나 내용 전체가 인용문일 경우 주로 사용한다.  
> q의 경우 인용문이 짧아서 간단하게 태그로 감싸서 표현할 때 사용한다.  
> 또한 인용문의 출처를 표시하기 위해서 cite 태그를 사용한다.

```html
<blockquote cite="http://www.naver.com">
  우리가 겪을 수 있는 가장 아름다운 체험은 신비다. <br />
  신비는 모든 참예술과 과학의 결과이다.
  <cite>알버트 아인슈타인</cite>
</blockquote>
<p>나는 말했다.<q>프론트엔드 개발자가 되고싶다고!</q></p>
```

**cite**는 태그 속 attr로 사용해서 출처를 표시할 수도 있고, 태그처럼 사용해서 기울어진 텍스트로 출처를 적어줄 수도 있다.  
**q**태그의 경우 태그로 감싼 부분에 인용문 표시 ""(큰 따옴표)가 생성된다.

### 7. 아무 의미 없는 태그(div, span)

> div, span은 다른 태그처럼 웹 페이지에서 어떤 기능을 담당하는 태그가 아니다.  
> 주로 작성된 문서의 요소들을 묶어서 처리하고 싶을 때(예를들어 CSS) 주로 사용한다.  
> 예를들어, span 태그는 텍스트를 감싸서 사용하면 그 부분만 효과를 적용할 수 있게 만들 수 있다.

### 8. form(form, input, button)

> **form**과 **input**과 **button**은 거의 같이 사용된다고 봐도 무방하다.  
> 우선 **form** 태그부터 살펴보도록 하자.
> **form**은 사용자로부터 **input**을 받기 위해 사용한다.

```html
<form action="API 주소" method="GET|POST"></form>
```

위와 같은 attr를 가지고 있는 태그이다.  
**action**은 사용자에게서 받은 input을 서버에 보내 처리하기 위한 속성으로, 이 데이터를 처리하기 위해 API 서버에 접근 가능한 URL을 적어줘야한다.  
**method**는 데이터를 보내는 방식으로, 데이터가 크면 POST, 작으면 GET을 사용한다고 생각하자.  
다음으로는 form 내부에서 사용할 input 태그에 대해서 알아보자.
input은 인풋, 인풋 필드(input field)라고 부르기도 한다.

```html
<input type="text" />
```

input 태그는 위와 같은 형태를 가진다.  
type이라는 attr에 어떤 것을 넣느냐에 따라 다양한 기능이 존재한다.

```html
<form action="" method="get">
  <input
    type="text"
    placeholder="안내 문구"
    maxlength="15"
    minlength="5"
    required
    value="초기값"
  />
  <input type="text" disabled />
  <input type="email" placeholder="이메일을 입력하세요" />
  <input type="password" placeholder="비밀번호" minlength="6" />
  <input type="url" placeholder="포트폴리오 URL을 적으시오" />
  <input
    type="tel"
    placeholder="전화번호 (***-****-****)"
    pattern="[0-9]{3}-[0-9]{4}-[0-9]{4}"
  />
  <input
    type="number"
    placeholder="나이를 입력하세요(12세  이상 ~  122세 이하)"
    min="12"
    max="122"
  />
  <input type="file" accept=".png, .jpg" />
</form>
```

첫 째, **text**일 경우에는 일반적인 텍스트 입력이 가능하다.  
둘 째, **email**일 경우에는 이메일 형식을 입력받는 칸을 생성한다. 따라서 @가 들어가 있는 이메일 형식이 아니라면 잘못된 형식이라는 경고문이 표시 된다.  
셋 째, **password**일 경우에는 비밀번호를 입력받는 칸을 생성한다. 여기에 입력되는 텍스트는 .표시로 표시된다.  
넷 째, **url**일 경우에는 http:// 와 같이 url을 입력할 수 있는 칸을 생성한다. 따라서 url 형식을 맞춰서 적지않으면 경고문이 표시 된다.  
다섯 째, **tel**일 경우에는 전화번호를 입력할 수 있다. 이 때 **pattern** 속성을 이용하여 [] 사이의 숫자를 {} 개 적도록 제한할 수 있다. **placeholder**와 함께 표시한 이 제한을 만족하지 못하면 경고문이 발생한다.  
여섯 째, **number**일 경우에는 숫자만을 입력할 수 있다. 여기서는 **min, max**를 통해서 최소, 최대 입력 가능 숫자 범위를 지정할 수 있다.  
일곱 째, **file**일 경우에는 파일을 제출할 수 있는 칸을 생성한다. 여기서 **accept**를 통해서 제출 가능한 파일 형식을 제한할 수도 있다.

위에서 언급된 attr을 제외하고는 기본적으로 아래의 attr이 공통적으로 쓰인다.  
**placeholder**로 안내 문구를 작성해줄 수 있다.  
**maxlength, minlength**를 통해 텍스트의 최대, 최소 길이를 제한 할 수도 있다. 주의할 점은 type이 **number**인 input에서는 **min, max**를 사용한다는 점이다.  
**value**를 통해 초기값을 먼저 기입해놓을 수 있다.  
**required**를 입력하면 해당 input에 반드시 값이 입력되야지 다음 동작을 진행 할 수 있다.  
반대로 **disabled**를 입력하면 해당 input에 아무것도 입력할 수 없게 막을 수 있다.

### 9. 레이블(label)

> **label**은 **input**에 대한 이름을 붙여준다.  
> 따라서 여러개의 input 중에서 어떤 input이 해당 label과 연결되는지 표시해줘야한다.  
> 그 기능을 담당하는게 **for** 속성이다. input의 id와 같은 값을 label의 for 속성에 입력해주면 해당 input과 label은 연결된다.  
> 이렇게 연결한 label을 클릭하면 마치 input을 클릭한 것 처럼 반응한다!

```html
<form>
  <label for="thisInput">레이블 실험</label>
  <input type="text" id="thisInput" placeholder="레이블 실험" />
  <button>submit</button>
</form>
```

위 코드에서 볼 수 있듯 id와 for가 같은 값을 가지고 있는 것을 볼 수 있다.  
이를 통해 해당 input과 label은 연결되었다.

사실 이렇게 label을 사용하는 이유는 8번에서 말한 input 태그의 또 다른 type과 관련이 깊다.  
input 태그의 또 다른 type으로는 **radio, checkbox**가 있다.

### 10. 선택(input - radio, checkbox)

> **radio**는 여러 개의 선택지 중 하나만 선택 가능한 input 태그의 type이다.

```html
<form action="" method="get">
  <input type="radio" id="hi" name="greeting" value="hello" />
  <label for="hi">hi</label>
  <input type="radio" id="bye" name="greeting" value="goodBye" />
  <label for="bye">bye</label>
  <hr />
  <input type="radio" id="anhi" name="angreeting" value="anhello" />
  <label for="anhi">anhi</label>
  <input type="radio" id="anbye" name="angreeting" value="angoodBye" />
  <label for="anbye">anbye</label>
  <button>submit</button>
</form>
```

만약 radio 버튼 중 하나가 선택되었는데 또 다른 radio 버튼이 다중 선택되는 것을 막기 위해서 input 태그에 **name** 속성을 사용힌다.  
**name** 속성이 같은 값을 가지면 그 태그들은 같은 그룹에 속한 것으로 인식이 되어서 다중 선택이 되는 것을 막을 수 있다.  
위 코드에서는 greeting 그룹과 angreeting 그룹으로 나눠져 있고 각각의 그룹에서는 다중 선택이 불가능하다.  
이러한 버튼들이 있는 form을 서버에 submit하면 어떤 name 그룹에 속한 어떤 radio가 선택되었는지를 서버에 보내는데, 문제는 그를 구분할 수 있는 방법이 없다는 것이다.  
따라서, input 태그에 **value** 속성을 사용하여 해당 radio의 고유한 이름을 붙여준다.  
이렇게 서버에 제출된 url은 **name = value & name = value** 가 붙어있게 된다.  
예를들어, hi와 anbye를 선택해서 서버에 제출하면 url에는 greeting = hello & angreeting = angoodbye가 붙어있을 것이다.

다음으로는 **checkbox** type을 살펴보자.

> **checkbox**는 여러 개의 선택지 중 여러 개를 선택 가능한 input 태그의 type이다.

```html
<form action="" method="get">
  <input type="checkbox" id="ko" name="lang" value="ko" />
  <label for="ko">한국어</label>
  <input type="checkbox" id="en" name="lang" value="en" />
  <label for="en">영어</label>
  <input type="checkbox" id="jp" name="lang" value="jp" />
  <label for="jp">일본어</label>
  <button>submit</button>
</form>
```

위 코드를 보면 알겠지만 **radio** 태그와 사용법이 완전히 동일하다.  
다른 점은 다중 선택이 가능하다는 점이다.
