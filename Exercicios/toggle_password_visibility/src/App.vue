<template>
  <div id="app">
    <div id="main">
      <Login />
    </div>
  </div>
</template>

<script>
import Titulo from './components/Title.vue';
import Login from './components/Login.vue';

export default {
  name: 'App',
  components: {
    Titulo,
    Login,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

#app {
  font-family: Arial, Helvetica, sans-serif;
  background: rgb(50, 134, 123);
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

#main {
  background: rgb(216, 216, 216);
  width: 60%;
  height: 80%;
  padding: 4px;
  border-radius: 8px;
  box-shadow: 4px 4px 8px rgb(66, 66, 66);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  
}
</style>
