# HTML 기초 정리

## 서버와 클라이언트
- **클라이언트(Client)**: 서버에게 요청하는 대상
- **서버(Server)**: 요청받은 서비스를 응답해주는 대상

---

## 웹(Web)
- 요청과 응답이 일어나는 장소

---

## 웹 브라우저(Web Browser)
- 사용자의 요청에 맞는 주소로 찾아가 인터넷 콘텐츠를 검색 및 열람
- 사용자에게 응답하기 위한 응용 프로그램의 총칭

---

## 프로토콜(Protocol)
- 네트워크 통신에서 통신을 하기 위한 규칙 또는 약속  
- 예: 사용자의 요청에 반드시 응답해야 함

### 주요 프로토콜
- **HTTP (Hypertext Transfer Protocol)**  
  클라이언트와 서버 간의 웹 페이지 등의 자원을 텍스트로 통신  
  > 가로채면 누구든 내용을 볼 수 있음

- **HTTPS (Hypertext Transfer Secure Protocol)**  
  자원을 공개키 암호화 방식으로 암호화해서 안전하게 통신

---

## IP(Internet Protocol)
- 네트워크 상에서 인터넷을 접속할 때 컴퓨터를 구별하기 위한 고유 번호

---

## DNS(Domain Naming Service)
- IP 주소는 기억하기 어렵기 때문에 이름을 부여할 수 있는 서비스

---

## WWW (World Wide Web)
- 인터넷에 연결된 전 세계 컴퓨터를 통해 정보를 공유할 수 있는 정보 공간

---

## W3C
- WWW를 위한 표준을 제정하고 관리하는 중립 기관

---

# 웹 표준(Web Standard)

## 1. HTML (Hypertext Markup Language)
- 화면의 기본 골조를 제작할 수 있는 마크업 언어
- **마크업 언어**: 태그를 이용해 문서나 데이터 구조를 기술

## 2. CSS (Cascading Style Sheets)
- HTML 문서의 스타일을 정의
- 내용과 스타일을 분리하여 유지보수 용이
- 역할: 레이아웃, 디자인 등

## 3. JavaScript (JS)
- 클라이언트에서 동작하는 스크립트 언어
- 역할: 이벤트 처리, 비동기 통신, 유효성 검사, 스타일/레이아웃 변경

## 4. XML (Extensible Markup Language)
- 데이터를 설명하기 위해 임의로 지은 태그로 감싸는 언어
- 목적: 데이터 전달
```xml
<?xml version="1.0"?>
<user>
   <user-id>hds1234</user-id>
   <name>한동석</name>
</user>
```

---

## HTML 요소
### 기본 구조
```html
<p> You are better </p>
<!-- 여는 태그 | 내용 | 닫는 태그 -->
```
### 속성(Attributes)
- 태그에 추가 정보를 담기 위해 사용
- 예: id, class 등

``` html
<p class="conversation" id="conv1"> You are much better </p>
```

### 속성 사용 시 주의사항

1. 태그 이름과 속성 사이, 속성들 사이에 공백 필요
2. 속성 이름 다음 등호(=) 작성
3. 속성 값은 따옴표 안에 작성 (생략 가능)
---

## HTML 요소의 종류

### 1. 블록 요소 (Block Elements)
- 예: `p`, `h1`~`h6`, `ul`, `ol`, `form`, `div` 등
- 특징:
  - 웹 페이지 상에 새로운 블록(영역)을 생성
  - 코드상에서 한 줄로 이어서 작성해도 화면에서는 아래줄로 내려감
  - 영역이 정확히 구분되어 `width`, `height`, `margin`, `padding` 속성 적용 가능

```html
<p>apple</p><p>banana</p>
```

화면 출력:  </br>
apple </br>
banana

---
### 2. 인라인 요소 (Inline Elements)
- 예: `span`, `a`, `img`, `strong`, `em` 등
- 특징:
  - 새로운 블록 영역을 생성하지 않고, 단락 내에 내용만 표시
  - 영역이 내용만큼만 차지하며, `width`와 `height` 설정 불가
  - `margin-top`, `margin-bottom`은 적용되지 않음
  - `padding`은 적용되지만 시각적으로 제한적

```html
<span>apple</span><strong>banana</strong>
```
화면 출력: </br>
applebanana

---

### 3. 인라인-블록 요소 (Inline-Block Elements)
- 예: `button`, `input`, `select` 등
- 특징:
  - 인라인 요소처럼 내용만큼의 영역을 가지면서, 블록처럼 고유 영역을 가짐
  - `width`, `height` 설정 가능
  - `margin`과 `padding` 모두 적용 가능
