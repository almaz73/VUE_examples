<template>
  <div>
    {{todo.text}}
    <button @click="$emit('remove', todo.id)">
      x
    </button>
  </div>
</template>
<script>
  export default {
    name: 'TodoListItem',
    props:{
      todo:{
        type:Object,
        required: true
      }
    }
  }
</script>
