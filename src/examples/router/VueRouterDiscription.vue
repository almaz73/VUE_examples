<template>
  <div>
    1) import VueRouter from 'vue-router' <br>
    2) установить в шабон строки < router-view > < /router-view ><br>
    3) подготовить страницы для переходов:
    <pre>
      var router = new VueRouter ({ routes: [
        {path: '/todoList', component: TodoList},
        {path: '/withComponent', component: WithComponent},
        {path: '/router', component: VueRouterDiscription}
      ]})
    </pre>
    4) Для удобства добавить ссылки на страницы:<br>
    < router-link to="/ссылка">{ { Название страницы } }< /router-link >

    <hr>
    Пример использования в компонентах HideMenu и App
  </div>
</template>
<script>
  export default {
    name: 'WueRouterDiscription'
  }
</script>
