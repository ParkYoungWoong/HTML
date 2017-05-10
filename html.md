# HTML

## HEAD (정보 콘텐츠)

base, title, meta, link, style, script, noscript

## SECTION (섹션 콘텐츠)

body, div, header, nav, section, article, main, aside, footer

## EMBEDED (외부 콘텐츠)



## HEADING (제목 콘텐츠)

## CONTENT (내용 콘텐츠)

## PARAGRAPH (문단 콘텐츠)

## EDIT (편집 콘텐츠)

## TABLE (표 콘텐츠)

## FORM (양식 콘텐츠)

## INTERACTIVE (상호작용 콘텐츠)


### `<!--...-->`

주석을 정의

### `<!DOCTYPE>`

도큐먼트 타입(문서형)을 정의

```html
<!DOCTYPE html>
```

### `<a></a>`

하이퍼링크를 정의

| Attribute | Value | Description |
|---|---|---|
| `href` | URL | 대상 URL 지정 |
| `target` | _self<br> _blank<br> _parent<br> _top | URL을 어디에 열 것인지 설정<br> - `_self` **기본값,** 현재 URL과 동일한 브라우징 컨텍스트에 로드<br> - `_blank` 새로운 브라우징 컨텍스트에 로드<br> - `_parent` 현재 URL의 상위 브라우징 컨텍스트에 로드, 부모가 없으면 '_self'와 동일<br> - `_top` URL을 최상위 레벨 탐색 컨텍스트에 로드, 부모가 없으면 '_self'와 동일 |
| `rel` | alternate<br> author<br> bookmark<br> external<br> help<br> license<br> next<br> nofollow<br> norefererr<br> noopener<br> prev<br> search<br> tag<br> | 현재 문서와 대상 URL 간의 관계를 지정<br> - `alternate` 현재 문서의 대체 표현을 제공<br> - `author` 현재 문서 작성자에게 링크 제공(작성자에게 e-mail(form) 보내기 등)<br> - `bookmark` 가장 가까운 조상 섹션(사이트 URL 등)에 대한 '[퍼머링크(permalink)](https://ko.wikipedia.org/wiki/%ED%8D%BC%EB%A8%B8%EB%A7%81%ED%81%AC)'를 제공<br> - `external` 현재 문서 사이트 외부로 이동<br> - `help` 상황 별 도움말에 대한 링크<br> - `license` 현재 문서에 대한 저작권 링크<br> - `next` 현재 문서가 시리즈의 일부로 참조된 문서가 현재의 다음 문서<br> - `nofollow` 참조된 문서를 보증하지 않음<br> - `norefererr` 다른 페이지로 이동할 때 페이지 주소 또는 다른 값을 HTTP 헤더를 통해 전송하지 않도록 함<br> - `noopener` 페이지가 window.opener를 악용!하지 못하도록 함<br> - `prev` 현재 문서가 시리즈의 일부로 참조된 문서가 현재의 이전 문서<br> - `search` 현재 문서 및 관련 페이지를 검색하는 데 사용할 수있는 리소스에 대한 링크를 제공<br> - `tag` 현재 문서에 적용되는 태그를 설명하는 문서를 참조 |
| `download` | 파일이름 | **HTML5,** 사용자가 'hyperlink'를 클릭할 때 대상을 다운로드 하도록 지정 |
| `media` | 미디어쿼리 | **HTML5,** 대상 URL이 어떤 미디어나 디바이스에 최적화되어 있는지 지정 |
| `type` | 미디어타입 | 대상 URL의 [미디어 유형](http://www.iana.org/assignments/media-types/media-types.xhtml)을 지정 |

```css
a {
  display: inline;
}
```

### `<abbr></abbr>`

약어(abbreviation, 준말)를 정의

> 약어를 'MarkUp'하면 브라우저, 번역 시스템 및 검색 엔진에 유용한 정보를 제공할 수 있습니다.

> `title` 속성을 사용하여 약어의 전체 단어를 표시하세요.

```html
The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.
```

```css
abbr {
  display: inline;
}
```

### `<address></address>`

문서 작성자나 소유자의 연락처 정보를 정의

> `<body></body>` 안에서는 문서의 연락처 정보를 나타냄

> `<article></article>` 안에서는 해당 'article'의 연락처 정보를 나타냄

```css
address {
  display: block;
}
```

### `<map></map>`

이미지 맵을 정의

| Attribute | Value | Description |
|---|---|---|
| `name` | 맵이름 | **필수,** `<img>`의 'usemap' 속성 값을 참조 |

```css
map {
  display: inline;
}
```

### `<area>`

이미지 맵의 영역을 정의

| Attribute | Value | Description |
|---|---|---|
| `shape` | default<br> rect<br> circle<br> poly | 영역의 모양을 지정 |
| `coords` | 좌표 | 영역의 좌표(coordinates)를 지정 |
| `href` | URL | 대상 URL 지정 |
| `alt` | 텍스트 | 대체 텍스트(alternate text)를 지정, `href` 속성이 있으면 필수! |
| `target` | _self<br> _blank<br> _parent<br> _top | URL을 어디에 열 것인지 설정<br> - `_self` **기본값,** 현재 URL과 동일한 브라우징 컨텍스트에 로드<br> - `_blank` 새로운 브라우징 컨텍스트에 로드<br> - `_parent` 현재 URL의 상위 브라우징 컨텍스트에 로드, 부모가 없으면 '_self'와 동일<br> - `_top` URL을 최상위 레벨 탐색 컨텍스트에 로드, 부모가 없으면 '_self'와 동일 |
| `hreflang` | 언어코드 | **HTML5,** 타겟 URL의 언어를 지정 |
| `rel` | alternate<br> author<br> bookmark<br> external<br> help<br> license<br> next<br> nofollow<br> norefererr<br> noopener<br> prev<br> search<br> tag<br> | 현재 문서와 대상 URL 간의 관계를 지정<br> - `alternate` 현재 문서의 대체 표현을 제공<br> - `author` 현재 문서 작성자에게 링크 제공(작성자에게 e-mail(form) 보내기 등)<br> - `bookmark` 가장 가까운 조상 섹션(사이트 URL 등)에 대한 '[퍼머링크(permalink)](https://ko.wikipedia.org/wiki/%ED%8D%BC%EB%A8%B8%EB%A7%81%ED%81%AC)'를 제공<br> - `external` 현재 문서 사이트 외부로 이동<br> - `help` 상황 별 도움말에 대한 링크<br> - `license` 현재 문서에 대한 저작권 링크<br> - `next` 현재 문서가 시리즈의 일부로 참조된 문서가 현재의 다음 문서<br> - `nofollow` 참조된 문서를 보증하지 않음<br> - `norefererr` 다른 페이지로 이동할 때 페이지 주소 또는 다른 값을 HTTP 헤더를 통해 전송하지 않도록 함<br> - `noopener` 페이지가 window.opener를 악용!하지 못하도록 함<br> - `prev` 현재 문서가 시리즈의 일부로 참조된 문서가 현재의 이전 문서<br> - `search` 현재 문서 및 관련 페이지를 검색하는 데 사용할 수있는 리소스에 대한 링크를 제공<br> - `tag` 현재 문서에 적용되는 태그를 설명하는 문서를 참조 |
| `download` | 파일이름 | **HTML5,** 사용자가 'hyperlink'를 클릭할 때 대상을 다운로드 하도록 지정 |
| `media` | 미디어쿼리 | **HTML5,** 대상 URL이 어떤 미디어나 디바이스에 최적화되어 있는지 지정 |
| `type` | 미디어타입 | 대상 URL의 [미디어 유형](http://www.iana.org/assignments/media-types/media-types.xhtml)을 지정 |

```html
<img src="planets.gif" width="145" height="126" alt="Planets" usemap="#planetmap">

<map name="planetmap">
  <area shape="rect" coords="0,0,82,126" href="sun.htm" alt="Sun">
  <area shape="circle" coords="90,58,3" href="mercur.htm" alt="Mercury">
  <area shape="circle" coords="124,58,8" href="venus.htm" alt="Venus">
</map>
```

```css
map {
  display: inline;
}
```

### `<article></article>`

**HTML5,** 독립적인 콘텐츠를 지정

> 문서, 페이지, 에플리케이션,  혹은 사이트 안에 독립적으로 구분되거나 신디케이션과 같은 재사용이 가능한 영역을 구성할 수 있습니다. 포럼의 글, 매거진/신문의 기사, 블로그 글, 혹은 기타 콘텐츠의 독립적인 항목이 될 수도 있습니다. 각각의 `<article>`은 구분 가능해야 하고, 일반적으로 제목 요소 (h1-h6)를 자식으로 포함하고 있습니다.

```css
article {
  display: block;
}
```

### `<aside></aside>`

**HTML5,** 주요 콘텐츠와 별개의 콘텐츠를 지정

```css
aside {
  display: block;
}
```

### `<audio></audio>`

**HTML5,** 사운드 콘텐츠를 지정

> `<audio>`와 `</audio>` 사이에 있는 텍스트는 `<audio>`를 지원하지 않는 브라우저에 표시됩니다.

| Browser | MP3 | Wav | Ogg |
|---|---|---|---|
| IE | O | X | X |
| CR | O | O | O |
| FF | O | O | O |
| SF | O | O | X |
| OP | O | O | O |

| Attribute | Value | Description |
|---|---|---|
| `autoplay` |  | 오디오가 준비되는 즉시 바로 실행 |
| `controls` |  | 오디오 컨트롤 표시 |
| `loop` |  | 반복 재생 |
| `muted` |  | 음소거 |
| `preload` | auto<br> metadata<br> none | 페이지 로드 시 오디오 로드 여부 설정,<br> - `none` 로드하지 않음<br> - `metadata` 메타데이터만 로드<br> - `auto` 전체 오디오 다운로드<br> - `빈 문자열` `auto`와 동일 |
| `src` | URL | 선택사항,<br> 오디오 파일의 URL 지정,<br> `<audio> 블록 내의 `<source>` 요소를 사용하여 포함될 오디오 지정 |

```html
<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
  Your browser does not support the audio tag.
</audio>
```

```css
audio {
  display: none;
}
```

### `<video></video>`

**HTML5,** 비디오 콘텐츠를 지정

| Browser | MP4 | WebM | Ogg |
|---|---|---|---|
| IE | O | X | X |
| CR | O | O | O |
| FF | O | O | O |
| SF | O | X | X |
| OP | O | O | O |

| Attribute | Value | Description |
|---|---|---|
| `autoplay` |  | 동영상이 준비되는 즉시 재생 시작 |
| `controls` |  | 비디오 컨트롤 표시 |
| `width` | px | 비디오 플레이어의 가로 너비 |
| `height` | px | 비디오 플레이어의 세로 너비 |
| `loop` |  | 반복 재생 |
| `muted` |  | 음소거 |
| `poster` | URL | 비디오가 다운로드되는 동안, 사용자가 재생 버튼을 누를 때까지 표시할 이미지 지정 |
| `preload` | auto<br> metadata<br> none | 페이지 로드 시 오디오 로드 여부 설정,<br> - `none` 로드하지 않음<br> - `metadata` 메타데이터만 로드<br> - `auto` 전체 오디오 다운로드<br> - `빈 문자열` `auto`와 동일 |
| `src` | URL | 선택사항,<br> 비디오 파일의 URL 지정,<br> `<video> 블록 내의 `<source>` 요소를 사용하여 포함될 비디오 지정 |

```css
video {
  display: inline;
}
```

### `<source>`

**HTML5,** 다양한 미디어의 리소스를 지정

| Attribute | Value | Description |
|---|---|---|
| `src` | URL | **필수,**<br> URL을 지정,<br> `<audio>`, `<video>`에 사용 |
| `type` | MIME 타입 | [MIME](https://developer.mozilla.org/ko/docs/Web/HTTP/Basics_of_HTTP/MIME_types) 타입을 설정 |

```css
source {
  display: inline;
}
```

### `<base>`

문서의 모든 상대 URL에 대한 기본 URL을 지정

> HTML Base 요소 (`<base>`) 는 문서에 포함된 모든 상대 URL들의 기준 URL을 나타냅니다. 한 문서에 하나의 `<base>` 요소만이 올수 있습니다.

> head 섹션의 다른 요소가 `<base>` 요소의 정보를 사용하도록 `<head>` 요소의 첫 번째 요소로 `<base>` 태그를 사용합니다.

| Attribute | Value | Description |
|---|---|---|
| `href` | URL | 상대 URL 주소들을 통해 사용될 기준 URL을 지정 |
| `target` | _self<br> _blank<br> _parent<br> _top<br> | 페이지 내 모든 URL을 어디서 열 것인지 설정<br> - `_self` **기본값,** 현재 URL과 동일한 브라우징 컨텍스트에 로드<br> - `_blank` 새로운 브라우징 컨텍스트에 로드<br> - `_parent` 현재 URL의 상위 브라우징 컨텍스트에 로드, 부모가 없으면 '_self'와 동일<br> - `_top` URL을 최상위 레벨 탐색 컨텍스트에 로드, 부모가 없으면 '_self'와 동일 |

### `<bdi></bdi>`

바깥 텍스트의 방향과 다르게 포맷될수 있는 일정 범위의 텍스트를 분리

> 포함된 텍스트의 방향을 알수 없을 때 내부의 텍스트의 방향이 고정되도록 하는데에 유용

```css
bdi {
  display: inline;  
}
```

| Browsers | CR | IE/EG | FF | SF | OP |
|---|---|---|---|---|---|
| Version | O | X | O | O | O |

### `<bdo></bdo>`

현재 텍스트 방향 지정 (bidirectional override, 양뱡향 치환)

| Attribute | Value | Description |
|---|---|---|
| `dir` | ltr<br> rtl<br> auto | **필수,**<br> `<bdo>` 요소 내부의 텍스트 방향을 지정<br> - right to left, left to right |

```css
bdo {
  display: inline;
}
```

### `<blockquote></blockquote>`

다른 출처에서 인용된 섹션

> 짧은(인라인) 인용문의 경우에는 `<q>` 사용

| Attribute | Value | Description |
|---|---|---|
| `cite` | URL | 인용된 정보의 원본 문서나 메세지를 가리키는 URL |

```css
blockquote {
  display: block;
}
```

### `<q></q>`

짧은 인용문을 지정

> 일반적인 브라우저에서는 앞뒤로 `""`(따옴표)가 붙음.
> reset.css 사용 시 초기화

| Attribute | Value | Description |
|---|---|---|
| `cite` | URL | 인용된 정보의 원본 문서나 메세지를 가리키는 URL |

```css
q {
  display: inline;
}
```

### `<body></body>`

문서의 본문을 정의

```css
body {
    display: block;
    margin: 8px;
}
```

### `<br>`

줄바꿈

> 단락을 구분할 때 사용하지 말아야 함

```css
br {
  display: inline;
}
```

### `<button></button>`

클릭 가능한 버튼을 지정

| Attribute | Value | Description |
|---|---|---|
| `name` | 이름 | 전송되는 버튼의 이름 |
| `type` | button<br> reset<br> submit | 버튼의 타입을 지정<br> - `button` 지정된 행위가 없는 일반 버튼<br> - `reset` 제어되고 있는 모든 값을 초기화<br> - `submit` 양식을 전송 |
| `value` | 텍스트 | 버튼의 초기값(양식에서 버튼 자체가 값을 제출하는 경우 사용) |
| `disabled` |  | 버튼을 비활성화 |
| `autofocus` |  | **HTML5,** 페이지가 로드될 때 자동으로 포커스 |
| `form` | form_id | **HTML5,** 동일한 문서 내 `<form>`의 id 속성값, 이 속성이 없는 경우는 `<button>`요소가 `<form>`의 자식 요소이여야 함 |
| `formaction` | URL | **HTML5,** 양식이 제출될 때 데이터를 보낼 위치 지정, `<form>`요소의 action 속성값을 덮어씀 |
| `formenctype` | application/x-www-form-urlencoded<br> multipart/form-data <br> text/plain | **HTML5,** 인코딩 방법 지정<br> - **기본값,** `application/x-www-form-urlencoded` 모든 문자는 전송 전 인코딩<br> - `multipart/form-data` 인코딩된 문자 없음(파일 업로드 컨트롤이있는 양식을 사용하는 경우 사용)<br> - `text/plain` 공백은 `+` 기호로 변환되지만 문자는 인코딩되지 않음 |
| `formmethod` | get<br> post | **HTML5,** 양식을 제출하기 위한 HTTP 메소드를 지정<br> [get, post 차이](http://www.letmecompile.com/get-post-%EB%B0%A9%EC%8B%9D-%EC%B0%A8%EC%9D%B4%EC%A0%90/) |
| `formnovalidate` |  | **HTML5,** 양식이 제출될 때 유효성 검사를 하지 않음 |
| `formtarget` | _self<br> _blank<br> _parent<br> _top | **HTML5,** 양식을 제출 후 응답을 표시할 위치를 설정<br> - `_self` **기본값,** 현재 URL과 동일한 브라우징 컨텍스트에 로드<br> - `_blank` 새로운 브라우징 컨텍스트에 로드<br> - `_parent` 현재 URL의 상위 브라우징 컨텍스트에 로드, 부모가 없으면 '_self'와 동일<br> - `_top` URL을 최상위 레벨 탐색 컨텍스트에 로드, 부모가 없으면 '_self'와 동일 |

```css
button {
  display: inline-block;
}
```

### `<canvas></canvas>`

**HTML5,** 스크립트를 이용하여 그래픽을 렌더링

> 그래픽 컨테이너로 실제 그래픽을 그리기 위해서는 스크립트를 사용해야 함

| Attribute | Value | Description |
|---|---|---|
| `width` | px | 캔버스의 가로 너비 |
| `height` | px | 캔버스의 세로 너비 |

```html
<canvas id="myCanvas"></canvas>

<script>
var canvas = document.getElementById("myCanvas");
var ctx = canvas.getContext("2d");
ctx.fillStyle = "#FF0000";
ctx.fillRect(0, 0, 80, 80);
</script>
```

```css
canvas {
  display: inline;
}
```

### `<caption></caption>`

테이블 설명을 정의

> `<caption>`는 `<table>`의 바로 뒤에 삽입해야 함,<br> 표당 하나의 캡션만 지정 가능

```html
<table>
  <caption>Monthly savings</caption>
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
</table>
```

```css
caption {
  display: table-caption;
}
```

### `<colgroup></colgroup>`

표 내부의 열을 정의

> 각 열보다는 전체 열을 정의할 때 유용

> `<colgroup>` 태그는 `<caption>` 요소 다음에 `<thead>`, `<tbody>`, `<tfoot>` 및 `<tr>` 요소 앞에 위치해야 함

| Attribute | Value | Description |
|---|---|---|
| `span` | 숫자 | **기본값 1,**<br> 연속적인 열의 수를 나타내는 양의 정수를 포함 |

```html
<table>
  <colgroup style="background-color:red"></colgroup>
  <tr>
    <th>ISBN</th>
    <th>Title</th>
    <th>Price</th>
  </tr>
  <tr>
    <td>3476896</td>
    <td>My first HTML</td>
    <td>$53</td>
  </tr>
</table>
```

```css
colgroup {
  display: table-column-group;
}
```

### `<col>`

`<colgroup>`요소 내에 각 열에 대한 속성을 지정

| Attribute | Value | Description |
|---|---|---|
| `span` | 숫자 | **기본값 1,**<br> 연속적인 열의 수를 나타내는 양의 정수를 포함 |

```html
<table>
  <colgroup>
    <col style="background-color:red">
    <col span="2" style="background-color:yellow">
  </colgroup>
  <tr>
    <th>ISBN</th>
    <th>Title</th>
    <th>Price</th>
  </tr>
  <tr>
    <td>3476896</td>
    <td>My first HTML</td>
    <td>$53</td>
  </tr>
</table>
```

```css
col {
  display: table-column;
}
```

### `<datalist></datalist>`

`<input>`요소에 대해 미리 정해진 옵션을 제공

```html
<input list="browsers">

<datalist id="browsers">
  <option value="Internet Explorer"></option>
  <option value="Firefox"></option>
  <option value="Chrome"></option>
  <option value="Opera"></option>
  <option value="Safari"></option>
</datalist>
```

```css
datalist {
  display: none;
}
```

| Browsers | CR | IE/EG | FF | SF | OP |
|---|---|---|---|---|---|
| Version | 20.0 | 10.0 | 4.0 | X | 9.0 |

### `<dl></dl>`

용어(`<dt>`)와 설명(`<dd>`)의 목록을 지정

> `<dt>`, `<dd>`를 같이 사용

```css
dl {
  display: block;
  margin-top: 1em;
  margin-bottom: 1em;
  margin-left: 0;
  margin-right: 0;
}
```

### `<dt></dt>`

용어를 지정

> `<dl>`, `<dd>`를 같이 사용

```css
dt {
  display: block;
}
```

### `<dd></dd>`

용어(`<dt>`)의 설명을 지정

> `<dl>`, `<dt>`를 같이 사용

```css
dd {
  display: block;
  margin-left: 40px;
}
```

### `<del></del>`

문서에서 삭제된 텍스트를 정의

> 삭제된 텍스트를 대신하여 삽입(추가)된 텍스트를 정의하기 위해서는 `<ins>` 사용

| Attribute | Value | Description |
|---|---|---|
| `cite` | URL | 텍스트가 삭제된 이유를 설명하는 문서 URL |
| `datetime` | YYYY-MM-DDThh:mm:ssTZD | 텍스트가 삭제된 시간 지정<br> - `YYYY` 년<br> - `MM` 월<br> - DD 일<br> - `T` or 스페이스 - 분리기호(시간이 있을 경우 사용)<br> - `hh` 시<br> - `mm` 분<br> - `ss` 초<br> - `TZD` 시간대 지정자(`Z` 그리니치 표준시) |

```html
<p>My favorite color is <del>blue</del> <ins>red</ins>!</p>
```

```html
<del datetime="2015-11-15T22:55:03Z">This text has been deleted</del>
```

```css
del {
  display: inline;
  text-decoration: line-through;
}
```

### `<ins></ins>`

문서에 삽입(추가)된 텍스트를 정의

> 삭제된 텍스트를 정의하기 위해서는 `<del>` 사용

| Attribute | Value | Description |
|---|---|---|
| `cite` | URL | 텍스트가 삽입(변경)된 이유를 설명하는 문서 URL |
| `datetime` | YYYY-MM-DDThh:mm:ssTZD | 텍스트가 삽입(변경)된 시간 지정<br> - `YYYY` 년<br> - `MM` 월<br> - DD 일<br> - `T` or 스페이스 - 분리기호(시간이 있을 경우 사용)<br> - `hh` 시<br> - `mm` 분<br> - `ss` 초<br> - `TZD` 시간대 지정자(`Z` 그리니치 표준시) |

```css
ins {
  display: inline;
  text-decoration: underline;
}
```

### `<details></details>`

**HTML,** 사용자가 보거나 숨길 수 있는 추가 세부 정보를 정의

> `<summary>`를 이용하여 세부사항의 머리글을 작성

| Attribute | Value | Description |
|---|---|---|
| `open` |  | **HTML5,** 세부 정보 표시 |

```html
<details open>
  <summary>Some details</summary>
  <p>More info about the details.</p>
</details>
```

```css
details {
  display: block;
}
```

| Browsers | CR | IE/EG | FF | SF | OP |
|---|---|---|---|---|---|
| Version | 12.0 | X | 49.0 | 6.0 | 15.0 |

### `<summary></summary>`

**HTML,** `<details>`의 보이는(visible) 머리글(제목)을 지정

> `<summary>`는 `<details>`의 첫번째 자식이어야 함

```css
summary {
  display: block;
}
```

| Browsers | CR | IE/EG | FF | SF | OP |
|---|---|---|---|---|---|
| Version | 12.0 | X | 48.0 | 6.0 | 15.0 |

### `<div></div>`

문서의 부분이나 섹션을 정의

```css
div {
  display: block;
}
```

### `<em></em>`

내용에서 약간의 강조(Emphasis)를 정의

```html
<p>나는 <em>당근</em>이 좋아!</p>
```

```css
em {
  display: inline;
  font-style: italic;
}
```

### `<i></i>`

특정 이유(전문용어, 기술용어, 관용적 표현, 생각 등)로 일반 글자와 구분(분리)을 위해 지정

```html
<p>그의 차는 매우 빠르기 때문에 그는 차에게 <i>번개</i>라는 이름을 지었다.</p>
```

### `<strong></strong>`

문장의 중요한 텍스트를 지정

```html
<p><strong>주의!</strong> 이것은 <strong>매우 위험</strong>합니다!</p>
```

```css
strong {
  display: inline;
  font-weight: bold;
}
```

### `<mark></mark>`

**HTML5,** 출처나 검색어와 같이 참조용으로 강조(사용자의 주의를 끄는) 표시된 텍스트를 지정

```html
<p><mark>HTML</mark>을 공부하세요.</p>
```

### `<cite></cite>`

작품의 제목(책, 노래, 영화, TV 프로그램, 그림, 조각품 등)을 정의

```html
<p><cite>The Scream</cite> by Edward Munch. Painted in 1893.</p>
```

```css
cite {
  display: inline;
}
```

### `<b>`

중요성이나 관련성이 없는 단순히 다른 문장과 구별되는 문체를 지정

> HTML 5 사양에 따르면 `<b>` 태그는 다른 태그가 더 적합하지 않을 때 마지막 수단으로 사용해야합니다.

```html
<p><b>폭스바겐 골프</b>는 도로 테스트에서 우승했다.</p>
```

```css
b {
  display: inline;
  font-weight: bold;
}
```

### `<dfn></dfn>`

용어(definition)의 정의 인스턴스

> `<dfn>` 의 부모 요소는 `<dfn>` 내부 용어에 대한 설명을 포함해야 함

```html
<p><dfn id="dfn-html" title="HyperText Markup Language">HTML</dfn>는 웹사이트를 제작하는 표준 언어입니다.</p>

<p><a href="#dfn-html">HTML</a>을 배우세요!</p>
```

```css
dfn {
  display: inline;
}
```

### `<code></code>`

컴퓨터 코드 구문을 정의

```css
code {
  display: inline;
}
```

### `<samp></samp>`

컴퓨터 프로그램의 샘플 출력물을 표시

```html
<p>다이어트 추적 앱이 <samp>"당신은 야채를 먹지 않는다."</samp> 라고 말했다.</p>
```

```css
samp {
  display: inline;
  font-family: monospace;
}
```

### `<kbd></kbd>`

키보드 입력 표시를 지정

> `ctrl`, `delete`, `shift` 등의 특정 키보드 키를 지정할 경우 사용

```html
<p><kbd>Cmd</kbd> + <kbd>R</kbd> 을 누르시오!</p>
```

```css
kbd {
  display: inline;
  font-family: monospace;
}
```

### `<var></var>`

수학적 표현이나 프로그래밍 문맥에서의 변수를 지정

```html
<p>간단한 방정식: <var>x</var> = <var>y</var> + 2</p>
```

```css
var {
  display: inline;
}
```
