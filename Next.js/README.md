# Next.js

### CSR Client Side Rendering

유저의 요청에 따라 필요한 부분만 데이터를 받아 랜더링

SPA(Single Page Application)

###### 특징

* Routing 관리 주체는 Front-end
* 사용자 친화적 (깜빡임 없이 부드러운 경험 유지)
* 필요한 데이터만 갱신해서 빠른 속도
* 서버 부하 감소
* AJAX + 리소스 다운로드로 초기 로딩 속도 느림
* SEO 불리 (검색엔진은 구글, 네이버 등 마다 다를 수 있음)


###### 동작방식

1. 유저가 페이지를 요청
2. HTML, CSS, JS를 한번에 다운로드 (TTV)
3. 다운로드 받은 JS가 데이터 요청
4. 랜더링 (TTV, TTI)

---------

### SSR Server Side Rendering

필요한 리소스를 서버에서 데이터까지 바인딩된 HTML을 전달

MPA(Multiple Page Application)

###### 특징

* SEO 유리
* 초기 로딩 속도는 빠르나 초반에 인터렉션은 불가 (TTV < > TTI 공백시간)
* 깜빡임
* 느린 페이지 로딩
* 서버로부터 만들어진 HTML을 받아서 전체 랜더링 (불필요한 부분까지 다시 랜더링)
* 서버 과부하

###### 동작방식

1. 유저가 페이지를 요청
2. 데이터 바인딩된 완성된 HTML 랜더링 (pre-rendering)
3. 유저 인터렉션 가능

----------

### 예시

| Render | Platform          | Objective                         |
|--------|-------------------|-----------------------------------|
| SSR    | 네이버 블로그           | SEO가 중요하기 때문에                     |
| SSR    | The NewYork Times | 초기 로딩이 빠르기 때문에 신문 기사를 빠르게 읽을 수 있음 |
| CSR    | 아고다               | 유저 인터렉션이 많기 때문에                   |


----------

React의 SSR 프레임워크 Next.js

Vue -> Nuxt

Angular -> 자체적으로 4버젼에 포함

Gatsby.js
