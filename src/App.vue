<template>
  <div id="app">
    <headerV />
    <toDoList />
  </div>
</template>

<script>
import toDoList from './components/toDoList.vue'
import headerV from './components/headerV.vue'

export default {
  name: 'app',
  data() {
    return {
      isActive: true
    }
  },
  components: {
    headerV,
    toDoList
  }
}
</script>

<style scoped>
    body {
    margin: 0px;
  }
</style>