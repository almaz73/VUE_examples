<template>
  <div>
    DinamicComponent
    <br>
<a href="#" @click="onChange('ComponentCircle')">Circle</a><br>
<a href="#" @click="onChange('ComponentSquare')">Square</a><br>
<a href="#" @click="onChange('ComponentTriangle')">Triangle</a><br>
    <component :is="currentComponent"></component>
  </div>
</template>
<script>
  import ComponentCircle from './ComponentCircle'
  import ComponentSquare from './ComponentSquare'
  import ComponentTriangle from './ComponentTriangle'
  export default{

    name:'WithComponent',
    components:{
      ComponentCircle,
      ComponentSquare,
      ComponentTriangle
    },
    data(){
      return{
        currentComponent:"ComponentCircle"
      }
    },
    methods:{
      onChange:function(val){
        this.currentComponent = val
      }
    }
  }
</script>
