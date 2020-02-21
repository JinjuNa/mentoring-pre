<template>
    <div class="sub_title">
        <img class="sub_effect" src="../../assets/sub_effect.png" alt="">
        <p class="title_text">VISION
            <!-- {{title.text}} -->
        </p>
    </div>
</template>

<script>
export default {
  name: 'Sub'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .sub_title{
      padding-top:75px;
      margin-left:255px;

  }

  .title_text{
      color: #3642c6;
      margin-top:10px;
      margin-left:225px;
      font-size: 40px;
      
  }
</style>
