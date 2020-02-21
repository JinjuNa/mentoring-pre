<template>
  <div class="sub">
    <SubTitle v-bind:titledata = "title"></SubTitle>
    <!--  -->
    <div class="recruit">
      <div class="contents">
        <h2><div class="icon_contact"><img src="../assets/icon_contact.png"></div></h2>
        <p>
        <span class="title">ADDRESS</span>
        서울시 마포구<br>
        <span class="title">TEL</span>
        010 0000 0000
        <span class="title">E-Mail</span>
        hello@gamil.com
        </p>
        <ul class="sns">
          <li><img src="../assets/sns01.png"></li>
          <li><img src="../assets/sns02.png"></li>
          <li><img src="../assets/sns03.png"></li>
          <li><img src="../assets/sns04.png"></li>
        </ul>
        <div class="map">
          <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3163.174502508647!2d126.9167315150405!3d37.55095227980089!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x357c98d081dd788f%3A0x1e1033abdff0efd9!2z7ISc6rWQ66as7LmY67mM!5e0!3m2!1sko!2skr!4v1581467708827!5m2!1sko!2skr" frameborder="0" style="border:0;" allowfullscreen=""></iframe>  
        </div>

      </div>
    </div>
  </div>
</template>

<script>
import SubTitle from './Sub/SubTitle'
export default {
  name: 'Contact',
  components : {
    SubTitle
  },
  data : function() {
return {
    title : "CONTACT"
  };
}
}
</script>
  
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
