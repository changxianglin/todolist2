<template>
  <div>
    <h1>root</h1>
    <todoList :todolists="todoLists" />
  </div>
</template>

<script>
import todoList from './components/todoList.vue';
export default {
  name: 'App',
  components: {
    todoList,
  },
  data() {
    return {
      todoLists: [
        {id: 1, task: '吃饭', isCompleted: true},
        {id: 2, task: '睡觉', isCompleted: false},
        {id: 3, task: '打豆豆', isCompleted: false},
      ]
    }
  }
}
</script>
