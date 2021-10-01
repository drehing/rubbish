<template>
  <div>
    <LeftSideBar/>
  </div>
  <Border/>
</template>

<script>
import LeftSideBar from './components/LeftSideBar.vue'
import Border from './components/Border.vue'

export default {
  name: 'App',
  components: {
    LeftSideBar,
    Border
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
