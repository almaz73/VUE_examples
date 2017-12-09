<template>
  <div>
    Данный пример показывает как добавлять и удалять элементы
    <TodoListInput
      v-model="inputText"
      @keydown.enter="addTodo"
    />
    <ul v-if="todos.length">
      <TodoListItem
        v-for="todo in todos"
        :key="todo.id"
        @remove="removeTodo"
        :todo = "todo"
      />
    </ul>
    <div v-else>Нет списка</div>
  </div>
</template>
<script>
  import TodoListInput from './TodoListInput'
  import TodoListItem from './TodoListItem'

  let number = 1
  export default {
    name: 'TodoList',
    components: {
      TodoListInput,
      TodoListItem
    },
    data () {
      return {
        inputText: '',
        todos: [
          {id: number++, text: "First"},
          {id: number++, text: "Second"},
          {id: number++, text: "Third"},
          {id: number++, text: "Forth"},
        ]
      }
    },
    methods: {
      addTodo: function () {
        console.log (" val = ", this.inputText);
        this.todos.push({
          id:number++,
          text:this.inputText
        })
        this.inputText = ''
      },
      removeTodo: function (id) {
        this.todos = this.todos.filter(todo =>{
          return todo.id !== id
        })
      }
    }
  }
</script>
