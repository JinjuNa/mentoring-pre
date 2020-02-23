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
        <carousel :per-page="1" :mouse-drag="true" >
          <slide>
            <img src="../../assets/slide1.png" class="pcSlider">
            <img src="../../assets/sliderM1.png" class="mobileSlider">
          </slide>
          <slide>
            <img src="../../assets/slide2.png" class="pcSlider">
            <img src="../../assets/sliderM2.png" class="mobileSlider">
          </slide>
          <slide>
            <img src="../../assets/slide3.png" class="pcSlider">
            <img src="../../assets/sliderM3.png" class="mobileSlider">
          </slide>
          <slide>
            <img src="../../assets/slide4.png" class="pcSlider">
            <img src="../../assets/sliderM4.png" class="mobileSlider">
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
  },
  mounted : function(){
    const ul = document.querySelector('.VueCarousel-dot-container'),
       btn= ul.querySelector('button');
       // eslint-disable-next-line no-console
       console.log(btn);

       btn.forEach((element, index) => {
         element.innerHTML = "0"+(index+1)
       })

    // btn.forEach((element,index) => {
    //     element.innerHTML = '0'+(index+1);
    // });
  }

}




</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.pcSlider{
  display: block;
}
  .mobileSlider{
    display: none;
  }

 
  /* .VueCarousel-dot-container .VueCarousel-dot:nth-child(1)::after{
    content: '1';
    display: block;
  } */

  @media all and (max-width:1023px){
    .mobileSlider{
      display: block;
    }

    .pcSlider{
      display: none;
    }


  }
</style>
