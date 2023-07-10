<template>
  <div>
    <h1>root</h1>
    <todoInput @addTask="addTask" />
    <todoList :todolists="todoLists"/>
    <todoButton :active="active" @changeActive="changeActive" />
  </div>
</template>

<script>
import todoList from './components/todoList.vue';
import todoButton from './components/todoButton.vue';
import todoInput from './components/todoInput.vue';
export default {
  name: 'App',
  components: {
    todoList,
    todoButton,
    todoInput,
  },
  data() {
    return {
      todoList: [
        {id: 1, task: '吃饭', isCompleted: true},
        {id: 2, task: '睡觉', isCompleted: false},
        {id: 3, task: '打豆豆', isCompleted: false},
      ],
      active: 0,
    }
  },
  computed: {
    todoLists() {
      if(this.active == 0) {
        return this.todoList
      } else if(this.active == 1) {
        return this.todoList.filter(item => item.isCompleted)
      } else {
        return this.todoList.filter(item => !item.isCompleted)
      }
    }
  },
  methods: {
    changeActive(index) {
      this.active = index
    },  
    addTask(val) {
      this.todoLists.push({
        id: this.todoLists.length + 1,
        task: val,
        isCompleted: false,
      })
    }
  }
}
</script>
