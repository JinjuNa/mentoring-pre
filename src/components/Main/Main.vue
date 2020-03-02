<template>
  <div class="main">
    <div class="wrap">
    <h1><router-link to="/"><img src="../../assets/logo.png" alt="메인로고"></router-link></h1>
    <div class="mainLink_wrap">
    <div class="mainLink blue">
        <p>Mentoring-lab에<br>대해 알고 싶으세요?</p>
        <div class="link">
          <router-link to="/">홈페이지</router-link>
        </div>
    </div>
    <div class="mainLink green">
        <p>꿈꾸는 많은 사람들과<br>소통해보고 싶으세요?</p>
        <div class="link">
            <a href="https://cafe.naver.com/mentoringlab">카페</a>
        </div>  
    </div>
    </div>
    </div>
    <Mainslider></Mainslider>
    
  </div>
</template>

<script>
import Mainslider from './MainSlider.vue'
import "../../style/main.css"
export default {
  name: 'Main',
  components : {
      Mainslider
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
