<template>
  <div class="mainSlider">
  <div class="mainSlider_wrap">
      <!-- <ul class="pager">
          <li><a href="#">01</a></li>
          <li><a href="#">02</a></li>
          <li><a href="#">03</a></li>
          <li><a href="#">04</a></li>
      </ul> -->

      <div class="slider">
        <carousel :per-page="1" :mouse-drag="true">
          <slide>
            <img src="../../assets/slide1.png">
          </slide>
          <slide>
            <img src="../../assets/slide2.png">
          </slide>
          <slide>
            <img src="../../assets/slide3.png">
          </slide>
          <slide>
            <img src="../../assets/slide4.png">
          </slide>
        </carousel>
      </div>
  </div>
  </div>
</template>

<script>
// import mainSlider from './components/MainSlider.vue'
import { Carousel, Slide } from 'vue-carousel';

export default {
  name: 'Mainslider',
  components : {
    Carousel,
    Slide
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


  @media all and (max-width:1023px){

  }
</style>
