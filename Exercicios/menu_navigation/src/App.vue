<template>
  <div id="app">
    <MenuBar />
  </div>
</template>

<script>
import MenuBar from './components/MenuBar.vue';

export default {
  name: 'App',
  components: {
    MenuBar,
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
