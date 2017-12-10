<template>
  <div id="app">
    <HideMenu/>
    <br><br><hr><br>

    <router-view></router-view>
  </div>
</template>

<script>
  import VueRouter from 'vue-router'
  import HideMenu from './components/HideMenu'

  import TodoList from './examples/list/TodoList'
  import WithComponent from './examples/with_component/WithComponent'
  import VueRouterDiscription from './examples/router/VueRouterDiscription'


  var router = new VueRouter ({
    routes: [
      {path: '/todoList', component: TodoList},
      {path: '/withComponent', component: WithComponent},
      {path: '/router', component: VueRouterDiscription}
    ]
  })

  export default {
    name: 'app',
    components: {
      HideMenu,
      TodoList,
      WithComponent
    },
    router: router
  }
</script>

<style>
  #app {
    position: relative;
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
  }
</style>
