<template>
  <div id="menu" @click="isPanelVisible = !isPanelVisible">
    &#65049; Примеры VUE : Menu &#65049;
    <div v-if="isPanelVisible">
      <ul v-for="menu in menus">
        <router-link :to="menu.link">{{menu.text}}</router-link>
      </ul>
    </div>
  </div>
</template>
<script>
  /**
   * Скрытая панель с Меню для перехода к примерам
   */
  export default {
    name: 'HideMenu',
    data () {
      return {
        isPanelVisible: false,
        tx: 'todoList',
        menus: [
          {link: 'todoList', text: " TodoList - добавление/удаление списка"},
          {link: 'withComponent', text: "..unconstruction"}
        ]
      }
    }
  }
</script>
<style scoped>
  #menu {
    position: absolute;
    border: 1px solid #ddd;
    border-radius: 5px;
    cursor: pointer;
    background: antiquewhite;
    padding: 5px;
    padding-right: 25px;
  }
</style>
