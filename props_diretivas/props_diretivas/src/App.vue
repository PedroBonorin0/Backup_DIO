<template>
  <div id="app">
    <Input v-model="text"/>
    {{ text }}
  </div>
</template>

<script>
// import ListItem from './ListItem.vue'; 
import Input from './Input.vue';

export default {
  name: 'App',
  components: { Input },
  data() {
    return {
      text: '',
    }
  },
  watch: {
    text(value) {
      text = (value);
    }
  }
};
</script>

<style>
*{
  margin: 0;
  padding: 0;
}

#app {
  font-family: Arial, sans-serif;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

button {
  padding: 2px;
  border: 1px solid black;
  margin: 3px;
  min-width: 80px;
}
</style>
