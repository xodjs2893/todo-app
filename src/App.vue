<template>
  <div id="app">
    <Header v-bind:title="pageTitle" />
    <AddTodo />
    <Todos v-bind:todos="todos"/>
  </div>
</template>

<script>
import Header from './components/layouts/Header'
import Todos from './components/Todos'
import AddTodo from './components/AddTodo'

export default {
  name: 'App',
  components: {
    Header,
    Todos,
    AddTodo
  },
  data(){
    return {
      pageTitle: "Todo 앱",
      todos: [
        { id: 1, title: "dentist", complete: false},
        { id: 2, title: "study", complete: true},
        { id: 3, title: "dinner", complete: false},
        { id: 4, title: "sleep", complete: true},
        { id: 5, title: "gogo", complete: false},
      ],
    };
  },
};
</script>

<style>
  *{
    box-sizing: border-box;
    padding: 0;
    margin: 0;
  }
</style>
