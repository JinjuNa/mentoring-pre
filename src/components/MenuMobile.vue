<template>
  <div class="menuMobile">
    <div class="menuButton" id="menuButtonM" v-on:click = "clickMenu">
      <span></span>
      <span></span>
      <span></span>
    </div>
    <div class="menuMobileWrap">
    <ul class="gnb" id="gnbM">
        <li>
            <a href="#/vision">VISION<div class="underline"></div></a>
        </li>
        <li>
            <a href="#/history">HISTORY<div class="underline"></div></a>
        </li>
        <li>
            <a href="#/program/school/vision">PROGRAM<div class="underline"></div></a>
            <ul class="subMenu">
                <li>
                    <a href="#/program/school/vision">스쿨과정<div class="underline"></div></a>
                </li>
                <li>
                    <a href="#/program/vivaldi">비발디<div class="underline"></div></a>
                </li>
                <li>
                    <a href="#/program/kgongvi">크공비<div class="underline"></div></a>
                </li>
                <li>
                    <a href="#/program/silkroad">실크로드<div class="underline"></div></a>
                </li>
            </ul>
        </li>
        <li>
            <a href="#/recruit">RECRUIT<div class="underline"></div></a>
        </li>
        <li>
            <a href="#/contact">CONTACT<div class="underline"></div></a>
        </li>
        <!-- <li v-bind:key="item.text" v-for="item in menu" >
          <router-link :to="item.url">{{item.text}}<div class="underline"></div></router-link>
        </li> -->
    </ul>
<!-- 
    <ul >
      <li v-bind:key="item.text" v-for="item in submenu" >
          <router-link :to="item.url">{{item.text}}<div class="underline"></div></router-link>
      </li>
    </ul> -->
    </div>
  </div>
</template>

<script>

window.onload = function(){
//   document.getElementById("menuButtonM").onclick = function(){
//     var gnb = document.getElementById("gnbM");
//     if(gnb.style.display == "none")
//       gnb.style.display = "block";
//     else
//       gnb.style.display = "none";
//   }

  const ul = document.querySelector('#gnbM');
  // if(!ul){
  //   return false;
  // }
  const li = ul.querySelectorAll('li');
  li.forEach(function(e){
    e.addEventListener('click', function(){
      ul.classList.remove('active');
    })
  })


}
export default {
  name: 'Menu',
  data : function() {
    return {
      menu : [
          {text : "VISION", url : "/vision"},
          {text : "HISTORY", url : "/history"},
          {text : "PROGRAM", url : "/program/school/vision"},
          {text : "RECRUIT", url : "/recruit"},
          {text : "CONTACT", url : "/contact"}
      ],
      submenu : [
        {text : "스쿨과정", url : "/program/school/vision"},
        {text : "비발디", url : "/program/vivaldi"},
        {text : "크공비", url : "/program/kgongvi"},
        {text : "실크로드", url : "/program/silkroad"}
      ]
    };
},
methods : {
  clickMenu : function(){
    var gnb = document.getElementById("gnbM");
      gnb.classList.toggle('active');
  }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .menuMobile{
        display: none;
        text-align: center;
        position: fixed;
        /* right: 16px;
        top: 20px; */
        width:100%;
        z-index: 10;
        margin-top:50px;

    }
  .menuButton{
    position: absolute;
    top:-35px;
    right: 20px;
    
  }
  .menuButton span{
    width:2.5rem;
    height: 4px;
    background-color: #000000;
    display: block;
    margin-bottom: 10px;
  }
.gnb{
    padding-top:50px;
}
  .gnb, .subMenu{
    z-index: 10;
  }
  .gnb{
    font-size: 1rem;
    letter-spacing: 0.305em;
    }
  .gnb>li{
    padding-bottom: 50px;

  }

  .gnb>li:nth-child(3){
      padding-bottom: 25px;
  }
  .gnb>li a{
    position: relative;
    
  }
  .underline{
    width:0;
    height: 15px;
    background-color: #c4f580;
    transition: all 1s;
    position: absolute;
    bottom: -3px;
    left: -5px;
    z-index: -1;
  }

  /* 폰트 모양, 크기에 따라서 left값 조정필요 */

  
.subMenu{
    margin-top:25px;
}
  .subMenu>li{
      height: 50px;
      line-height: 50px;
  }

  #gnbM{
    opacity: 0;
    transition: opacity 0.2s ease-in-out;
    background-color: white;
  }
  #gnbM.active{
    opacity: 1;
    /* display: block; */
    /* animation: fade-in 1s; */
  }

  @media all and (max-width:1023px){
    .menuMobile{
      display: block;
    }
    .menuButton span{
      width:25px;
      height: 3px;
      margin-bottom: 6px;
    }
    .subMenu{
        background-color: #eeeeee;
    }

    /* .gnb>li:nth-child(1):hover>a>.underline{
    width: 92px;
  }

  .gnb>li:nth-child(2):hover>a>.underline{
    width: 117px;
  }

  .gnb>li:nth-child(3)>a:hover>.underline{
    width: 130px;
  }

  .gnb>li:nth-child(4):hover>a>.underline{
    width: 117px;
  }

  .gnb>li:nth-child(5):hover>a>.underline{
    width: 130px;
  } */
  }
</style>
