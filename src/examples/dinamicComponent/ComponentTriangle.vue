<template>
  <div class="triangle"></div>
</template>
<script>
  export default{
    name:'ComponentTriangle'
  }
</script>
<style scoped>
  .triangle{
    width: 0px;
    height: 0px;
    border: 50px solid white;
    border-top: 0px;
    border-bottom: 100px solid blue;
  }
</style>
