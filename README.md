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

### 11. 옵션 선택(select, option)

> **select**는 다양한 **option** 중 하나를 선택할 수 있도록 풀다운 메뉴를 만들어 준다.  
> 풀다운 메뉴에는 **option** 태그를 사용하여 만든 텍스트들이 표시된다.

```html
<form action="" method="get">
  <label for="langSelect">언어</label>
  <select name="lang" id="langSelect">
    <option value="ko">ko</option>
    <option value="en">en</option>
    <option value="jp">jp</option>
  </select>
  <select multiple name="skill" id="skill">
    <option value="html">html</option>
    <option value="css">css</option>
    <option value="js">js</option>
  </select>
  <button type="submit">submit</button>
</form>
```

**multiple** 속성을 추가하면 cmd나 ctrl을 누른채로 다중 선택이 가능하도록 만들 수도 있다.

### 12. textarea

> 일반적인 **input**태그가 한 줄 정도의 입력을 받아낼 수 있다면, **textarea**는 여러 줄의 input을 받을 수 있다.

```html
</form>
    <label for="field">field</label>
    <textarea
      name=""
      id="field"
      cols="30"
      rows="10"
      placeholder="자기소개를 입력하세요"
    ></textarea>
```

**cols**와 **rows** 속성을 사용하여 행과 열의 최대치를 설정할 수 있다.  
또한, **placeholder** 속성을 사용하여 안내 문구를 적을 수도 있다.  
여타 input과 마찬가지로 **label**과 연결을 할 수도 있다.

### 13. 버튼(button)

> **button** 태그는 위에서부터 **form, input** 태그와 함께 많이 쓰여왔다.  
> **button** 태그를 사용할 때는 항상 **type** attr를 반드시 써줘야한다.  
> attr에는 3가지가 있다.  
> 첫 째, **submit**이다. 보통 **form**을 제출할 때 사용한다. 가장 많이 사용하는 속성이기도 하다.  
> 둘 째, **button**이다. 보통 JS와 연결해서 눌렀을 때 JS 코드가 실행되게 하는 등의 기능을 구현할 때 쓰인다.  
> 셋 째, **reset**이다. **form, input**에 기입한 내용을 전부 리셋해버리는 기능을 구현한다.

```html
<form action="">
  <input type="text" />
  <!--type attr을 꼭 적어줘야한다!-->
  <!--form을 제출할 때 사용-->
  <button type="submit">버튼1</button>
  <!--눌렀을 때 js 실행되게 하는 등의 기능할 때 쓴다.-->
  <button type="button">버튼2</button>
  <!--form 등을 리셋하고 싶을 때 사용-->
  <button type="reset">버튼3</button>
</form>
```

### 14. 표(table, tr, th, td, thead, tbody, tfoot)

> 데이터를 담은 표를 테이블이라고 한다.  
> 리스트와 비슷한 느낌으로 태그를 사용한다고 생각하면 쉽다.  
> **table**을 만들겠다고 하고, **tr, th, td** 태그를 활용하여 자식요소를 생성한다.  
> **tr == table row**를 의미한다. 즉, 테이블의 한 행을 생성해주며, 이 태그 안에 작성하는 것들은 모두 한 행에 표시된다.  
> **th == table head**를 의미한다. 이 태그 안에 작성하는 것은 bold체로 작성되며, 해당 행이나 열을 대표하는 것을 작성할 때 사용한다. 따라서 첫번째 **tr**에서 **th**를 몇 개 정의하냐에 따라 다음 행에 작성할 코드의 개수가 정해지게 될 것이다.  
> **td == table data**를 의미한다. 하나의 셀에 들어갈 데이터를 입력하는 태그이다.

```html
<table>
  <thead>
    <tr>
      시작
      <th>ID</th>
      <th>이름</th>
      <th>개발분야</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>00001</td>
      <td>박기영</td>
      <td>프론트엔드</td>
    </tr>
    <tr>
      <td>00002</td>
      <td>김아무개</td>
      <td>풀스택</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>2아이디</td>
      <td>2명</td>
      <td>2직군</td>
    </tr>
  </tfoot>
</table>
```

위 코드를 보면 **thead, tbody, tfoot** 태그가 **table** 관련 태그들을 감싸고 있는 것을 확인할 수 있다.  
이들은 브라우저가 html 파일을 읽을 때 어떤 부분이 head인지 어떤 부분이 body인지 어떤 부분이 foot인지 더 명확하게 구분할 수 있게 만들어준다.  
보통 **thead**의 경우 header 역할을 하는 **th**가 모여 있는 부분을 감싼다.  
**tbody**의 경우 body 역할을 하는 **td**가 모여 있는 부분을 감싼다. 물론 해당 행에서의 역할에 따라 **th**가 감싸질 수도 있다!  
**tfoot**의 경우 총 합계 같은 최종 결론 데이터를 감쌀 때 사용한다.

### 14 - 1. 테이블 활용 예시

> 아래와 같은 시간표 테이블을 예제로 만들어보았다.  
> 이해하는데 큰 도움이 되었으므로 길더라도 한번쯤 보는게 좋을 것 같다.  
> CSS 부분은 무시하고 HTML 파트만 보도록 하자.

<img width="798" alt="스크린샷 2022-02-06 오전 1 34 48" src="https://user-images.githubusercontent.com/86224851/152650297-6308787b-4c2b-43b9-8714-65b57efbd25b.png">

```html
<table>
  <thead>
    <tr>
      <th></th>
      <th scope="col">월</th>
      <th scope="col">화</th>
      <th scope="col">수</th>
      <th scope="col">목</th>
      <th scope="col">금</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <th scope="row">1교시</th>
      <td rowspan="2" class="html-css-basic">왕초보 HTML &amp; CSS</td>
      <td class="coding">모각코</td>
      <td rowspan="2" class="html-css-basic">왕초보 HTML &amp; CSS</td>
      <td class="coding">모각코</td>
      <td rowspan="2" class="html-css-basic">왕초보 HTML &amp; CSS</td>
    </tr>
    <tr>
      <th scope="row">2교시</th>
      <td rowspan="2" class="js-skillup">JavaScript 스킬업</td>
      <td rowspan="2" class="js-skillup">JavaScript 스킬업</td>
    </tr>
    <tr>
      <th scope="row">3교시</th>
      <td class="js-basic">JavaScript 시작반</td>
      <td class="js-basic">JavaScript 시작반</td>
      <td class="js-basic">JavaScript 시작반</td>
    </tr>
    <tr>
      <th scope="row" colspan="6">점심 시간</th>
    </tr>
    <tr>
      <th scope="row">4교시</th>
      <td class="sass-basic">SASS 기초반</td>
      <td rowspan="2" class="portfolio">
        HTML &amp; CSS<br />
        포트폴리오반
      </td>
      <td rowspan="2">Open Seminar</td>
      <td rowspan="2" class="portfolio">
        HTML &amp; CSS<br />
        포트폴리오반
      </td>
      <td class="sass-basic">SASS 기초반</td>
    </tr>
    <tr>
      <th scope="row">5교시</th>
      <td class="coding">모각코</td>
      <td class="coding">모각코</td>
    </tr>
  </tbody>
</table>
```

우선, 시간표에서는 요일이 중요한 지표로 사용되므로 요일 행을 **tr**로 생성한 후 각각의 요일을 **th**로 처리해주었다. 또한, 이들의 집합이 테이블의 헤더 역할을 할 것이므로 **thead**로 감싸주었다. 총 6개의 셀을 생성했으므로 다음 행부터는 6개의 셀을 만들어야 테이블이 정상적으로 만들어질 것이다.  
다음 행으로 넘어가기 전에 **scope**라는 attr을 볼 수 있다. 이 속성은 헤더가 어떤 방향을 대표하는지를 알려준다. value가 **col**인 것을 보면 해당 열을 대표하는 헤더라는 것을 알 수 있다.

다음으로는 각 교시에 맞는 시간표를 만들 것이므로 본격적인 데이터가 작성될 곳이라 생각하여 **tbody**를 사용해 감싸주었다. 몇 교시인지 알려주는 부분은 그 행을 대표하는 헤더 역할을 하므로 **th**태그를 사용하였고, **scope** attr의 value를 **row**로 설정했다.  
월요일에는 1-2교시가 같은 과목이므로 두 개 행의 공간을 차지하게 만들어줘야하는데, 이런 셀 병합 동작을 지원하는 attr이 바로 **rowspan, colspan**이다. **rowspan**을 2로 설정하여 행 2칸을 하나로 병합한 것을 확인할 수 있다.

이렇게 셀 병합을 진행하게 되면, 다음 행에서 작성하는 데이터들이 자동적으로 밀려나게 된다. 따라서 셀 병합을 진행한 행의 다음 행을 작성할 때는 병합된 셀 개수만큼 데이터를 빼고 작성해야 정상적인 모양이 나온다.  
예를들어, 2교시 파트를 보면, 1교시에서 **rowspan**을 사용해 2번째 행을 이미 선점하고 있으므로 이 공간은 사용할 수 없게 된다. 따라서 데이터가 2개만 작성된 것을 볼 수 있다.  
이런 식으로 **rowspan, colspan**이 사용된 경우 데이터 개수를 알맞게 계산하여 작성해야한다.

점심시간의 경우 하나의 행을 전부 사용하고 있으므로, 해당 행의 모든 열을 병합하면 된다. 열 병합은 앞서 말했듯 **colspan**을 사용하면 된다. **thead**에서 6개의 **th**를 만들었으므로 모든 칸은 통합하려면 **colspan**을 6으로 설정하면 될 것이다.

### 15. 미디어(img, audio, video, iframe)

> **img** 태그는 이미 앞에서 충분히 다뤘으므로 **audio, video, iframe**를 살펴 보자.  
> 우선, **audio**는 음성 파일을 입력할 떄 쓰는 태그이다.  
> 기본 형태는 아래와 같다.

```html
<audio src=""></audio>
```

**source** attr에 상대경로를 입력해서 파일을 불러오면 된다.  
다만, 이 상태로 태그를 입력해도 웹 페이지에는 전혀 보이지않고 들리지도 않는다.  
이 때 필요한 것이 **controls** attr이다.  
이 속성을 사용하면 볼륨 조절, 재생 시간 등을 확인 할 수 있다.

```html
<audio src="" controls></audio>
```

만약 이런 볼륨 조절, 재생 시간 같은 표시를 보고싶지않고, 재생은 하고 싶다면  
**autoplay** attr을 사용하면 된다.

```html
<audio src="" autoplay></audio>
```

이런 오디오 파일을 계속해서 재생하고 싶다면 **loop** attr을 사용하면 된다.

```html
<audio src="" loop></audio>
```

이렇게 하나의 태그로 사용하는 방법도 있지만, 여러개의 파일은 삽입하는 방법도 있다.  
아래와 같이 작성하는 것이 그 방법이다.

```html
<audio>
  <source src="./assets/audios/kimbug.wav" type="audio/wav" />
  <source src="./assets/audios/kimbug.mp3" type="audio/mpeg" />
  <source src="./assets/audios/kimbug.ogg" type="audio/ogg" />
  <p>당신의 브라우저를 버리시고 크롬을 사용하시는게 어떨까요?</p>
</audio>
```

이 방법은 어떤 파일 확장자를 지원하지 않는 브라우저에서 동작을 원활하게 하기 위한 것으로, 특정 브라우저에서 지원하지 않는 파일 확장자가 있다면 **source** 태그에 링크되어 있는 파일들 중 지원하는 파일을 재생한다.  
또한, 반드시 **type** attr을 같이 사용해야하는데, **"audio/파일 확장자 코드"** 를 작성해주면 된다.  
파일 확장자 코드의 경우 확장자마다 상이하니 검색해서 적는 것이 좋을 것 같다.  
만약, 이렇게 적어놓은 파일들 중 해당 브라우저에서 지원하는 파일 확장자가 단 하나도 없다면, 위 코드 예시처럼 다른 태그를 사용하여 안내 문구를 보이도록 할 수 있다.

> 다음으로는 **video** 태그이다.  
> **video** 태그는 **audio** 태그와 사용법이 사용법이 완전히 같다.

```html
<video src="" controls></video>
<video autoplay>
  <source src="./assets/videos/kimbug.mp4" type="video/mp4" />
  <source src="./assets/videos/kimbug.mov" type="video/mp4" />
  <p>당신의 브라우저를 업데이트 하는게 어떨까요?</p>
  <a href="https://browsehappy.com/">브라우저 업데이트 하기</a>
</video>
```

여기서 눈여겨 볼 점은 **source** 태그를 감싼 **video**에 **autoplay** attr을 사용했다는 것이다. 이 방법은 **audio** 태그와도 사용법이 같으니 눈여겨 보자.

> 다음으로는 **iframe** 태그이다.  
> 이 태그는 html 안에 또 다른 html을 임베드할 떄 쓰인다.

```html
<iframe src="" frameborder=""></iframe>
```

**source** attr에 보여주고싶은 url이나, html 파일의 상대 경로를 적으면 된다.  
보통은 **iframe**을 직접 작성하기보다 유튜브 같은 영상의 **iframe** 코드를 가져와서 사용한다.  
예를들어 어떠한 유튜브 영상의 **iframe** 코드를 가져오 결과는 아래와 같다.

```html
<iframe
  width="560"
  height="315"
  src="https://www.youtube.com/embed/0_pvO4oDI64"
  title="YouTube video player"
  frameborder="0"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen
></iframe>
```

많은 속성들이 이미 설정되어 있는 것을 볼 수 있다.  
위 코도는 영상만을 띄워준다.

### 16. 기타 태그

> 이번에는 쏠쏠하게 활용되는 태그를 몇 가지 살펴보도록 하겠다.  
> 첫 째, **abbr** 태그이다.  
> abbreviation을 의미하며 번역하면 약자라는 의미를 가진다.  
> 어떤 약자에 대한 설명을 하고 싶을 때 그 약자를 이 태그로 감싸주면 된다.

```html
<p>
  너...혹시
  <abbr title="Attention Deficit Hyperactivity Disorder">ADHD</abbr>니?
</p>
```

반드시 **title** 속성을 같이 사용해줘야하며, 약자의 풀 네임을 적어준다.  
태그로 감싸진 부분은 점선으로 밑줄이 쳐지며, 마우스를 올리면 **title**에 적어놓은 풀 네임이 보이게 된다.

> 둘 째, **address** 태그이다. 주로 연락처에 관한 정보를 입력할 때 쓰는 태그이다.  
> 연락처라고 하면 다음과 같은게 있을 것이다.

- (물리적 주소) 번지수, 위도, 경도..
- URL
- E-mail
- 전화번호
- SNS

```html
<address>
  <h1>박갓디바</h1>
  <a href="https://youtube.com/c/kimbug">https://youtube.com/c/kimbug</a>
</address>
```

이렇게 **address** 태그 안에 적은 텍스트들은 폰트가 기울어져서 나오게 된다.

> 셋 째, **pre, code** 태그이다. **pre**는 preformatted text를 의미한다.  
> 즉, 포맷되기 전 날 것의 텍스트를 말한다.
> **code**는 말 그대로 코드를 의미하며, 무조건 **pre** 태그와 같이 써야하는 것은 아니다.  
> 주로 코드를 보여주고싶을 때 사용한다.

```html
<p>예를들어, p태그는 엔터를 써도 웹에 표시되지않지만</p>
<pre>
      그냥 이렇게 쓰면
      내가 html에 작성한 그대로
      출력이 된다.
심지어 탭 키 마저 구현이 됨.
ㅇ ㅏ ㄴ ㅕ ㅎ ㅏ ㅅ ㅔ ㅇ
 ㄴ    ㅇ            ㅛ
<p>ㅇ ㅏ ㄴ ㅕ ㅎ ㅏ ㅅ ㅔ ㅇ
  ㄴ    ㅇ            ㅛ</p>
  이렇게 써도 pre 내부에서는 그대로 출력
  <code>
    console.log('hello ki0');
      let ki0 = 100;
  </code>
  </pre>
<code> console.log('hello ki0'); let ki0 = 100; </code>
```

위 코드처럼 **p** 태그는 엔터를 코드에 아무리 입력을 해도 결국 웹 페이지에 보이는 것은 한 줄로 된 텍스트인데, **pre** 태그를 사용하면 이런 표현이 전부 웹 페이지에 그대로 보이게 되는 것이다. 또한 폰트에도 변화가 생긴다.  
**code** 태그는 **pre** 안에 작성한게 있고, 밖에 작성한게 있다.  
둘의 차이점은 엔터나 탭 같은 코드 가시성을 높여주는 것들이 적용이 되냐 안되냐이다.  
**pre** 태그 안에 작성한 **code**는 입력한 텍스트 그대로 출력되는 반면, 밖에 작성한 **code**는 **p** 태그처럼 아무리 엔터를 입력해도 하나의 줄로 보이게 된다.

### 17. HTML 기본 골격

아무것도 작성하지 않은 상태의 HTML 코드를 보며, 어떤 부분이 어떤 역할을 하는지 살펴보자.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <!--뇌라고 생각하자.-->
    <!--굉장히 중요한 많은 정보를 가지고 있음.-->
    <!--meta 데이터를 선언할 때 사용됨.-->
    <!--어떤 문서가 참조되었고 등등..-->
    <meta charset="UTF-8" />
    <!--meta 태그는 name = "메타데이터 종류, 성격", content ="메타데이터 값"-->
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <!--viewport는 화면 크기라고 생각하면 됨. 화면 전체가 viewport 사이즈가 됨. 최근에는 브라우저를 보는 화면, 기기 크기가 너무 다양해서 중요한 속성이 됨. 반응형 사이트를 만들 수 있게 됨!!!-->
    <!--width=device-width : width 값을 사용자 화면의 가로 사이즈에 맞춰라~-->
    <!--initial-scale=1.0 : 원래 사이즈 비율로 보여줘라~-->
    <meta name="author" content="Rki0" />
    <meta name="keywords" content="Rki0, html 기초, html 공부" />
    <!--키워드에 작성된 녀석들을 검색하면 우리 페이지를 보여줘~라고 부탁하는 것-->
    <meta
      name="description"
      content="이 페이지는 박기영의 프론트엔드 기초 공부를 위한 실험 사이트입니다."
    />
    <!--description은 설명한다는 것으로, 이 페이지가 무엇에 관한 페이지인지 주절주절 설명함.-->
    <title>
      <!--문서의 대제목 역할. 웹 페이지의 제목이므로, 검색 최적화(Search Engine
      Optimization)에 매우 중요한 역할!--> <!--검색 최적화를 위해 title을 잘
      쓰는 법! 1. 키워드 단순 나열은 비추천! 2. 페이지마다 그에 맞게 변경.
      예를들어, 포폴 사이트가 있다면 홈, 자기소개, 작품 페이지 등등...다르게!
      무엇에 관한 내용인지 센스있게 적자~ --> HTML의 기본 골격 공부
    </title>
    <link rel="stylesheet" href="./style.css" />
    <!--css 파일을 링크하는 태그. 아래 처럼 font를 사용할 때도 link 태그를 사용함.-->
    <link
      href="https://spoqa.github.io/spoqa-han-sans/css/SpoqaHanSansNeo.css"
      rel="stylesheet"
      type="text/css"
    />
    <style>
      /*html 문서 내에서 css 코드를 작성할 때 사용. 굳이...?*/
      /*link로 연결한 css 파일을 덮어버리기 때문에 웬만하면 사용하지말자.*/
      h1 {
        font-size: 3em;
      }
    </style>
  </head>
  <body>
    <!--우리가 지금까지 배운 태그를 적는 곳-->
    <!--웹 문서에 보여줄 모든 컨텐츠를 담는 곳-->
    <h1>Ki0</h1>
    <p>안녕하세요 폰트입니다.</p>
    <script src="">
      /*js파일을 연결할 때 쓰는 태그*/
    </script>
    <script>
      /*이렇게 사용하면 html 문서 내에서 js 코드를 바로 적을 수 있음. style 태그와 같다.*/
      /*script 태그는 다운로드 될 때 까지 html 동작을 중지하고 있으므로 head보다는 body 가장 아래에 작성하는 편.*/
      let name = document.querySelector("h1");
      name.addEventListener("click", function (event) {
        this.innerText = "hi";
      });
    </script>
  </body>
</html>
```

가정 먼저 보게되는 태그는 **DOCTYPE**이다. 이 태그는 뒤에 파일 형식을 붙여줌으로서 이 파일이 어떠한 기능을 할 파일인지를 알려준다.  
Document Type Declaration == DTD 선언 == 문서 형식 선언 이라고도 한다.  
위 코드에서는 html이라고 적었으므로 "이 문서는 HTML5(가장 최신 버전)으로 작성된 문서니까 잘 렌더링 해줘~"라고 브라우저에게 알려주는 것이다.

다음으로는, **html** 태그이다. 이 태그부터 html 문서가 시작된다는 것을 알려준다.  
이 태그 안에는 **head, body** 태그가 큰 덩어리로 들어간다.

**head** 태그는 말 그대로 문서의 뇌를 담당한다.
