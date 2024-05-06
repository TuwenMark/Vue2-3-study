<template>
  <!-- 输入框 -->
  <header class="header">
    <h1>小黑记事本</h1>
    <input
      placeholder="请输入任务"
      class="new-todo"
      v-model.trim="toDoName"
      @keyup.enter="handleAdd"
    />
    <button class="add" @click="handleAdd">添加任务</button>
  </header>
</template>

<script>
export default {
  data() {
    return {
      toDoName: '',
    }
  },
  methods: {
    handleAdd() {
      if (this.toDoName === '') {
        alert("请输入正确的任务名称")
        return
      }
      this.$emit('add', this.toDoName)
      this.toDoName = ''
    },
  },
}
</script>

<style></style>
