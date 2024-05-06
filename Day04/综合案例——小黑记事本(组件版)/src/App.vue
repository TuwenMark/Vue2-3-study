<template>
  <!-- 主体区域 -->
  <section id="app">
    <ToDoHeader @add="handleAdd" />
    <ToDoMain :list="list" @del="handleDel" />
    <ToDoFooter :list="list" @clear="handleClear" />
  </section>
</template>

<script>
import ToDoHeader from './components/ToDoHeader.vue'
import ToDoMain from './components/ToDoMain.vue'
import ToDoFooter from './components/ToDoFooter.vue'
export default {
  components: {
    ToDoHeader,
    ToDoMain,
    ToDoFooter,
  },
  data() {
    return {
      list: JSON.parse(localStorage.getItem('list')) || [
        { id: 1, name: '打篮球' },
        { id: 2, name: '看电影' },
        { id: 3, name: '逛街' },
      ],
    }
  },
  methods: {
    handleAdd(toDoName) {
      this.list.unshift({
        id: +new Date(),
        name: toDoName,
      })
    },
    handleDel(id) {
      this.list = this.list.filter((item) => item.id != id)
    },
    handleClear() {
      this.list = []
    },
  },
  watch: {
    list: {
      deep: true,
      handler(newValue) {
        localStorage.setItem('list', JSON.stringify(newValue))
      }
    }
  }
}
</script>

<style></style>
