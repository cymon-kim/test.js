<template>
<header>
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
    <img alt="Vue logo" src="./assets/logo.png">
    
    <div class="menu">
     <label for="expand-menu"><div>메뉴</div></label>
     <input type="checkbox" id="expand-menu" name="expand-menu">
     <ul>
        <li><a href="#" class="item"><div>프로필</div></a></li>
        <li><a href="#" class="item"><div>데이터사용량</div></a></li>
        <li><a href="#" class="item"><div>내URL</div></a></li>
        <li><a href="#" class="item"><div>구매내역</div></a></li>
        <li><a href="#" class="item"><div>추천목록</div></a></li>
        <li><a href="#" class="item"><div>설정</div></a></li>
     </ul>
    </div>
    
</header>

 




</template>

<script>

export default {
  name: 'App',
  // 변수 선언 data(){return{변수명 : 변수,}},
  data(){
    return{
      데이터 : 0,
    }
  },

  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.menu ::before{
    font-family: 'Material Icons';
    font-size: 1.5em;
    float: left;
    clear: left;
}
.menu label::before{ content: '\e5d2'; }
.menu li:nth-child(1) a::before{ content: '\f02e'; }
.menu li:nth-child(2) a::before{ content: '\e8d6'; }
.menu li:nth-child(3) a::before{ content: '\e88a'; }
.menu li:nth-child(4) a::before{ content: '\e8cc'; }
.menu li:nth-child(5) a::before{ content: '\e87d'; }
.menu li:nth-child(6) a::before{ content: '\e8b8'; }


#expand-menu { /* 체크박스 폼 요소 감춤 */
    display: none;
}
#expand-menu:checked ~ ul { /* 체크박스 체크되었으면 메뉴 목록 표시 - 반응형 표시용 */
    display: block;
    height: auto;
}

.menu {
    display: block;
    width: 200px;
    background-color: #000;
    color: #fff;
    border-radius: 20px;
    padding: 10px;
    box-sizing: border-box;
    overflow: hidden; /* 반응형 애니메이션용 */
    transition: all 0.5s ease; /* 반응형 애니메이션 */
}
.menu ul {
    list-style: none;
    margin: 0;
    padding: 0;
}
.menu a, .menu > label {
    display: block;
    height: 25px;
    padding: 8px;
    cursor: pointer;
    color: #fff;
    text-decoration: none;
}

.menu a:hover {
    color: #000;
}
.menu ul li:hover, .menu > label:hover {
    background-color: #fff;
    color: #000;
    border-radius: 10px;
}
.menu div {
    line-height: 1.5;
    font-size: 1em;
    font-family: 'Noto Sans KR';
    padding: 0 0 0 50px; /* 아이콘과 텍스트 사이 여백 */
}
@media screen and (max-width:1023px) {
    .menu { /* 1단계 */
        width: 60px;
    }
}
@media screen and (max-width:560px) {
    .menu #expand-menu:not(:checked) ~ ul { /* 2단계 */
        display: none;
    }
}
.menu div {
    position: absolute; /* 절대 위치로 텍스트 고정 */
    left: 50px;
    line-height: 1.5;
    font-size: 1em;
    font-family: 'Noto Sans KR';
    padding: 0 0 0 20px; /* 패딩 20p로 축소 */
}
</style>
