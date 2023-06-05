## Image Gallery Optimization

유동균, '웹 개발 스킬을 한 단계 높여 주는 프론트엔드 성능 최적화 가이드', 제 4장 이미지 갤러리 최적화 기반의 실습 및 요약 레포지토리입니다. 크롬 개발자 도구의 Performace, Lighthouse, Network 패널을 이용하여 성능 측정 후 최적화 작업을 진행하였습니다.

## Getting Started

#### install dependencies

```
$ npm install
or
$ yarn
```

#### start development server

```
$ npm run start
or
$ yarn start
```

#### start json-server

```
$ npm run server
or
$ yarn server
```

#### build + serve

```
$ npm run serve
or
$ yarn serve
```

## Problems - Solutions

- [x] Layout Shift

## `Layout Shift`

```html
<div class="wrapper">
  <img class="image" src="..." />
</div>
```

```css
/* Intrinsic aspect ratio 16:9 */

/* Method 1 */
.wrapper {
  position: relative;
  width: 160px;
  paddign-top: 56.25%;
}
.image {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
}

/* Method 2 */
.wrapper {
  width: 100%;
  aspect-ratio: 16 / 9;
}
.image {
  width: 100%;
  height: 100%;
}
```
