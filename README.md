# portfolio_m
[모바일 포트폴리오 바로 가기](https://cyber-steer.github.io/portfolio_m) <br>

# 사용한 css framework
[jquery mobile](https://jquerymobile.com/) <br>
[Apache ECharts](https://echarts.apache.org/en/index.html) <br>
[bootstrap](https://getbootstrap.com/) <br>
[materializecss](https://materializecss.com/) <br>
[bulma](https://bulma.io/) <br>
[pure.css](https://purecss.io/) <br>

# 사이트맵

![레이아웃](https://github.com/cyber-steer/portfolio_m/blob/main/media/img/markdown/sitemap.png)

# 화면
![레이아웃](https://github.com/cyber-steer/portfolio_m/blob/main/media/img/markdown/view.png)

# 페이지별 css framework 사용 현황
- index.html
  + jquery mobile
- info.html
  + jquery mobile
- project.html
  + jquery mobile
  + bootstrap
- profile.html
  + jquery mobile
  + materializecss
- about.html
  + jquery mobile
  + bootstrap
- skills.html
  + jquery mobile
  + bulma
  + pure.css
  + Apache ECharts
- connect.html
  + jquery mobile
  + bulma
  + bootstrap

# jquery mobile css 사용
```html
<div data-role="page">
    <div data-role="panel">
    </div>
    <div data-role="header">
    </div>
    <div data-role="content">
    </div>
    <div data-role="footer">
    </div>
</div>
```
모든 페이지에서 기본적으로 jquery mobile 구조를 사용

# Apache ECharts 사용
![레이아웃](https://github.com/cyber-steer/portfolio_m/blob/main/media/img/markdown/chart.png)
```html
<div id="Language" style="width: 80vw;height:400px; margin: 0 auto;"></div>
```
```javascript
let chartDom = document.getElementById('Language');
let myChart = echarts.init(chartDom);
let option;
option = {
    tooltip: {
        trigger: 'axis',
        axisPointer: {
        type: 'shadow'
        }
    },
    grid: {
        left: '3%',
        right: '4%',
        bottom: '3%',
        containLabel: true
    },
    xAxis: [
        {
        type: 'category',
        data: ['C', 'Java', 'Python', 'Javascript'],
        axisTick: {
            alignWithLabel: true
        }
        }
    ],
    yAxis: [
        {
        type: 'value'
        }
    ],
    series: [
        {
        name: 'Direct',
        type: 'bar',
        barWidth: '60%',
        data: [30, 60, 65, 60]
        }
    ]
};
option && myChart.setOption(option);
```
[참조](https://echarts.apache.org/examples/en/editor.html?c=bar-tick-align) <br>


# bootstrap 사용

![레이아웃](https://github.com/cyber-steer/portfolio_m/blob/main/media/img/markdown/project_bootstrap.png)

```html
<div class="container text-center">
    <div class="row">
        <div class="col-sm-4">
        </div>
        <div class="col-sm-4">
        </div>
        <div class="col-sm-4">
        </div>
    </div>
</div>
```
가장 큰 div가 가운데 정렬을 시켜주고 <br>
class가 row인 div안에 col-sm-4를 넣어줍니다 <br>
row는 한 행을 뜻하며 col-sm-4는 행의 크기를 12로 잡고 셀 크기를 4/12만큼 잡으며 셀 크기가 575px이하가 되면 자동으로 다시 레이아웃을 정렬하는 반응형 웹 구조입니다
[참조](https://getbootstrap.com/docs/5.2/layout/grid/) <br>

```html
<div class="card">
    <div class="embed-container" style="">
        <img src="..." class="card-img-top" alt="...">
    </div>
    <div class="card-body">
        <h5 class="card-title">카드 이름</h5>
        <p class="card-text">카드 내용</p>
        <a href="#" class="btn btn-primary" style="color: white;">버튼 이름</a>
    </div>
    </div>
</div>
```
카드를 만들어주는 css components입니다

[참조](https://getbootstrap.com/docs/5.2/layout/grid/) <br>

# materialize 사용

![레이아웃](https://github.com/cyber-steer/portfolio_m/blob/main/media/img/markdown/profile_materialize.png)

```html
<div class="nav-content">
    <ul class="tabs tabs-transparent">
        <li class="tab"><a class="active" href="profile.html">Profile</a></li>
        <li class="tab"><a href="about.html">About Me</a></li>
        <li class="tab"><a href="skills.html">Skills</a></li>
        <li class="tab"><a href="connect.html">Connect</a></li>
    </ul>
</div>
```
탭 형식의 네이게이션입니다
class에 active를 추가함으로 현재 선택되어 있는 항목을 표시할수 있습니다

[참조](https://materializecss.com/navbar.html) <br>

```html

<div class="row">
    <div class="col s12"> 12/12</div>
</div>
<div class="row">
    <div class="col s6 title">6/12</div>
    <div class="col s6">6/12</div>
</div>
```
materialize에서 지원하는 grid입니다

[참조](https://materializecss.com/grid.html) <br>

![레이아웃](https://github.com/cyber-steer/portfolio_m/blob/main/media/img/markdown/about_materialize.png)
```html
<div class="divider"></div>
<div class="section">
    <h5>Section 1</h5>
    <p>Stuff</p>
</div>
<div class="divider"></div>
<div class="section">
    <h5>Section 2</h5>
    <p>Stuff</p>
</div>
<div class="divider"></div>
    <div class="section">
    <h5>Section 3</h5>
<p>Stuff</p>
</div>
```
divider가 선을 그려주고
section안에 h5가 제목 p가 내용입니다

[참조](https://materializecss.com/grid.html) <br>

# bulma 사용
![레이아웃](https://github.com/cyber-steer/portfolio_m/blob/main/media/img/markdown/skills_bulma.png)
```html
<progress class="progress" value="15" max="100">15%</progress>
```
퍼센트 바를 꾸며주는 방법입니다

[참조](https://bulma.io/documentation/elements/progress/) <br>

![레이아웃](https://github.com/cyber-steer/portfolio_m/blob/main/media/img/markdown/content_bulma.png)
```html
<div class="columns">
    <div class="column is-4">
    </div>
    <div class="column is-4">
    </div>
    <div class="column is-4">
    </div>
</div>
```
bulma에서의 grid 사용 방법입니다
[참조](https://bulma.io/documentation/columns/sizes/) <br>

```html
<div class="card">
    <div class="card-content">
    <div class="media">
        <div class="media-left">
        <figure style="margin: 0;">
            <span class="bi bi-phone"></span>
        </figure>
        </div>
        <div class="media-content">
        <p class="title is-4">연락처</p>
        <p class="subtitle is-6">@010-5296-7638</p>
        </div>
    </div>
    </div>
</div>
```
bulma에서 카드 사용법입니다
[참조](https://bulma.io/documentation/columns/sizes/) <br>


# fure 사용
![레이아웃](https://github.com/cyber-steer/portfolio_m/blob/main/media/img/markdown/skills_fure.png)
```html
<div class="pure-menu pure-menu-horizontal">
    <ul class="pure-menu-list">
        <li class="pure-menu-item pure-menu-selected">
            <a href="#" class="pure-menu-link">Selected</a>
        </li>
        <li class="pure-menu-item">
            <a href="#" class="pure-menu-link">Normal</a>
        </li>
        <li class="pure-menu-item pure-menu-disabled">
            <a href="#" class="pure-menu-link">Disabled</a>
        </li>
    </ul>
</div>
```
메뉴를 꾸며주는 fure의 방법입니다

[참조](https://purecss.io/menus/) <br>

# icon 사용법
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.9.1/font/bootstrap-icons.css">

<span class="bi bi-phone"></span>
```
css파일을 불러와서 class에 원하는 아이콘을 적으면 됩니다
[아이콘 목록](https://cyber-steer.github.io/icon-list.html) <br>
