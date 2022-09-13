<template>
  <div id="app">
    <PriceTab />
  </div>
</template>

<script>
import PriceTab from './components/PriceTab.vue'

export default {
  name: 'App',
  components: {
    PriceTab,
    
    }
}
</script>

<style>
*{
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
  font-weight: bold;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
}
</style>
