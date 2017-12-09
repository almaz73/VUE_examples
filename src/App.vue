<template>
  <div id="app">
    <h4>Примеры VUE :
        <router-link to="/todoList">TodoList</router-link>
        <router-link to="/withComponent">| WithComponent</router-link>
      <hr>
    </h4>


    <router-view></router-view>
  </div>
</template>

<script>
import TodoList from './examples/list/TodoList'
import WithComponent from './examples/with_component/WithComponent'
import VueRouter from 'vue-router'

var router = new VueRouter({
  routes:[
    {path:'/todoList', component: TodoList},
    {path:'/withComponent', component: WithComponent},
  ]
})

export default {
  name: 'app',
  components: {
    TodoList,
    WithComponent
  },
  router: router
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
