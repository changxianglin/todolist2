<template>
<ul class="list-group">
  <li class="list-group-item d-flex justify-content-between align-items-center">
    <!-- 复选框 -->
    <div class="form-check">
      <input class="form-check-input" type="checkbox" value="" id="defaultCheck1">
      <label class="form-check-label" for="defaultCheck1">
        Default checkbox
      </label>
    </div>
    <span class="badge badge-primary badge-pill">已完成</span>
    <span class="badge badge-warning badge-pill">未完成</span>
  </li>
</ul>
</template>

<script>
export default {
  name: 'todoList',
}
</script>

<style scoped>
  .list-group {
    width: 500px;
    margin: 0 auto;
  }
</style>