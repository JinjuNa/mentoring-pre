<template>
    <div class="sub_title">
        <img class="sub_effect" src="../../assets/sub_effect.png" alt="">
        <p class="title_text">
            {{titledata}}
        </p>
    </div>
</template>

<script>
export default {
  name: 'SubTitle',
  props : ['titledata']
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
      /* margin-top:10px; */
      margin-left:150px;
      font-size: 40px;
      
  }

  .sub_effect{
      width:150px;
  }

  @media all and (max-width:1023px){
      .title_text{
          font-size: 17.5px;
          margin-left:0;
      }

      .sub_title{
          padding-top: 0;
          margin-left:0;
          text-align: center;
      }

      .sub_effect{
          width:55px;
      }
  }
</style>
