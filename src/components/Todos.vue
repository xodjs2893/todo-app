<template>
  <div>
      <div v-for="todo in todos" v-bind:key="todo.id">
          <TodoItem v-bind:todo="todo" />
      </div>
  </div>
</template>

<script>
import TodoItem from './TodoItem'
export default {
    components:{
        TodoItem,
    },
    props:{
        todos: Array,
    },
};
</script>

<style>

</style>