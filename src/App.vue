<template>
  <div>
    <h1>root</h1>
    <todoList />
  </div>
</template>

<script>
import todoList from './components/todoList.vue';
export default {
  name: 'App',
  components: {
    todoList,
  }
}
</script>
