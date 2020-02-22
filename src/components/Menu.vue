<template>
  <div class="menu">
    <div class="menuButton" id="menuButton" v-on:click = "clickMenu">
      <span></span>
      <span></span>
      <span></span>
    </div>
    <ul class="gnb" id="gnb">
        <li v-bind:key="item.text" v-for="item in menu" >
          <router-link :to="item.url">{{item.text}}<div class="underline"></div></router-link>
        </li>
    </ul>

    <ul class="subMenu">
      <li v-bind:key="item.text" v-for="item in submenu" >
          <router-link :to="item.url">{{item.text}}<div class="underline"></div></router-link>
      </li>
    </ul>
  </div>

</template>

<script>

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
       var gnb = document.getElementById("gnb");
    if(gnb.style.display == "none")
      gnb.style.display = "block";
    else
      gnb.style.display = "none";
    }
  }
}

window.onload = function(){
  alert("hi");
  const ul = document.querySelector('.gnb');
  const li = ul.getElementsByTagName('li');
  const sub = document.querySelector('.subMenu')
  li[2].addEventListener('click', function(){
    alert("hi");
    sub.style.display == "block";
  })
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .menuButton{
    float:right;
    position: relative;
    z-index: 99;
    cursor: pointer;
    
  }
  .menuButton span{
    width:2.5rem;
    height: 4px;
    background-color: #000000;
    display: block;
    margin-bottom: 10px;
  }

  .gnb, .subMenu{
    z-index: 10;
    position: relative;
  }
  .gnb{
    font-size: 18px;
    letter-spacing: 0.305em;
    }
  .gnb>li{
    margin-bottom: 50px;
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

  .gnb>li:nth-child(1):hover .underline{
    width: 92px;
  }

  .gnb>li:nth-child(2):hover .underline{
    width: 117px;
  }

  .gnb>li:nth-child(3):hover .underline{
    width: 130px;
  }

  .gnb>li:nth-child(4):hover .underline{
    width: 117px;
  }

  .gnb>li:nth-child(5):hover .underline{
    width: 130px;
  }

  .subMenu{
    display: none;
    position: absolute;
    top:200px;
    left:-80px;
    font-size:18px;
  }

  .subMenu li{
    margin-bottom: 25px;
  }

  @media all and (max-width:1023px){
    .menu{
      display: none;
    }
    /* .menuButton span{
      width:25px;
      height: 3px;
      margin-bottom: 6px;
    }
    .gnb{
      display: none;
    }

    .subMenu{
      display: none;
    } */
  }
</style>
