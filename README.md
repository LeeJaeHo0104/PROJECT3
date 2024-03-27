# 현대 캐피탈 💸

> 현대 캐피탈 홈페이지를 **클론코딩하여 구현한** 프로젝트 입니다.
> 
> 배포화면 보기 [_사이트 보기_](https://leejaeho0104.github.io/PROJECT3/). 
> 
## 목차
- [현대 캐피탈 💸](#현대-캐피탈-)
  - [목차](#목차)
- [프로젝트 소개](#프로젝트-소개)
  - [기술스텍](#기술스텍)
  - [주요구현사항](#주요구현사항)
  - [해당 프로젝트를 통해 배운점](#해당-프로젝트를-통해-배운점)
  - [폴더 구조](#폴더-구조)
  - [아웃라인](#아웃라인)
  - [브라우저 호환성](#브라우저-호환성)
  - [Contact](#contact)


# 프로젝트 소개
- 현대 캐피탈 홈페이지를 클론코딩하여 제작한 웹사이트입니다.
- 100% 스스로 작업한 프로젝트 입니다.
- html5, css3, Scss, 자바스크립트, JQuery를 사용해 구현한 웹사이트입니다.


## 기술스텍
<img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
<img src="https://img.shields.io/badge/css3-1572B6?style=for-the-badge&logo=css3&logoColor=white">
<img src="https://img.shields.io/badge/scss-CC6699?style=for-the-badge&logo=sass&logoColor=white">
<img src="https://img.shields.io/badge/JS-F7DF1E?style=for-the-badge&logo=javascript&logoColor=white">
<img src="https://img.shields.io/badge/jquery-0769AD?style=for-the-badge&logo=jquery&logoColor=white">


## 주요구현사항
- **Scss**만을 활용하여 제작
- 바닐라 자바스크립트를 이용한 숫자 증가 애니메이션 구현
- JQuery를 이용한 FadeInOut 배너 제작


## 해당 프로젝트를 통해 배운점

```javascript
1. 숫자 증가 애니메이션
- if,setInterVal, clearInterVal 함수를 이용하여 설정한 숫자에 도달하면 실행이 종료되는 함수를 구현하였다.
- 변수 play의 주어진 false값을 이용하여 scroll 이벤트가 발생하더라도 1회 실행 이후 실행되지 않는 방법을 배웠다.
- 이러한 과정을 통해 if문의 실행 여부를 적절하게 조절하는법을 알게 되었다.

//프로그램 내 구현한 코드입니다.
let play = false;

window.onscroll = function() {
	let height = window.pageYOffset;

  const country = document.querySelector('#country');
	const money = document.querySelector('#money');
	const people = document.querySelector('#people');
	let countC = 0;
	let countM = 0;
	let countP = 0;

	if (!play && height > 2400) {
		play = true;
		let countingC = setInterval(function () {
			if (countC == 14) {
				clearInterval(countingC);
				return false;
			}
			countC += 1;
			country.innerHTML = new Intl.NumberFormat().format(countC);
		}, 50);
		let countingM = setInterval(function () {
			if (countM == 130) {
				clearInterval(countingM);
				return false;
			}
			countM += 1;
			money.innerHTML = new Intl.NumberFormat().format(countM);
		}, 10);
		let countingP = setInterval(function () {
			if (countP == 5300) {
				clearInterval(countingP);
				return false;
			}
			countP += 10;
			people.innerHTML = new Intl.NumberFormat().format(countP);
		}, 1);
	}
}
```


## 폴더 구조

폴더는 아래와 같은 구조로 제작되었습니다.
```
root
└── index.html
│
└── scss
│    ├── index.scss
│    ├── base
│    │    ├── _base.scss
│    │    └── _typo.scss
│    ├── components
│    │    ├── _banner.scss
│    │    ├── _button.scss
│    │    ├── _nav.scss
│    │    └── _popup.scss
│    └── layout
│    │    ├── _footer.scss
│    │    └── _main.scss
└── css
│    ├── index.css
│    └── index.css.map
└── dist
│    ├── index.min.css
│    └── index.min.css.map
│
└── js
│    ├── script.js
│
└── img
```

## 아웃라인
index html파일은 아래와 같은 구조로 제작되었습니다.
```
body
  └── header
  │    ├── nav
  │    └── banner
  └── main
  │    ├── section1
  │    ├── section2
  │    ├── section3
  │    ├── section4
  │    ├── section5
  │    └── section6
  └──footer
       ├── footer_nav
       └── address
```

## 브라우저 호환성
|브라우저|![chrome_icon](https://github.com/LeeJaeHo0104/PROJECT__1/assets/151009272/3e912b12-1d18-4635-8f9c-9abba81cfb80)|![edge_icon](https://github.com/LeeJaeHo0104/PROJECT__1/assets/151009272/f494434e-b0bd-447f-a3b1-6e7fc9e41d17)|![firefox_icon](https://github.com/LeeJaeHo0104/PROJECT__1/assets/151009272/6da83ea9-6744-422a-8929-a771dd20d94a)|![opera_icon](https://github.com/LeeJaeHo0104/PROJECT__1/assets/151009272/1fa4b9c9-9aa6-467f-bbc6-1fc46959c053)
|---|---|---|---|---|
|호환성 여부|O|O|O|O|


## Contact
- 이름 : 이재호
- 연락처 : 010-5351-5294
- 이메일 : ljh2735294@naver.com