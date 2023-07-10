<template>
<div class="input-group mb-3">
  <div class="input-group-prepend">
    <span class="input-group-text" id="basic-addon1">新建任务</span>
  </div>
  <input type="text" class="form-control" placeholder="请输入任务" aria-label="Username" aria-describedby="basic-addon1" v-model="taskname">
  <button type="button" class="btn btn-primary" @click="sumbmit">提交任务</button>
</div>
</template>

<script>
export default {
  name: 'todoInput',
  data() {
    return {
      taskname: '',
    }
  },
  emits: ['addTask'],
  methods: {
    sumbmit(){
      this.$emit('addTask', this.taskname)
      this.taskname = ''
    }
  }
}
</script>

<style scoped>
  .input-group {
    width: 500px;
    margin: 0 auto;
  }
</style>