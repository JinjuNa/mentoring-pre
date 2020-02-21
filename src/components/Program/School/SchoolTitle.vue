<template>
  <div class="schoolTitle">
    <p>SCHOOL PROCESS</p>
    <h3>{{titledata.text}}</h3>
    <img :src="titledata.img" :alt="titledata.text">
  </div>
</template>

<script>

export default {
  name: 'SchoolTitle',
  props : ['titledata']
}
</script>
  
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .schoolTitle{
        text-align: center;
        margin-top:70px;
        margin-bottom:30px;
    }

    .schoolTitle p{
      font-size: 13px;
      color:#c4f580;
    }

    .schoolTitle h3{
      font-size: 25px;
      color:#3642c6;
      margin-bottom:40px;
    }
</style>
