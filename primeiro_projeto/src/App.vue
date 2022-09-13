<template>
  <div id="app">
    <Title v-if="shouldAppear"/>
    <button @click="shouldAppear = false">Click</button>
    {{ count }}
  </div>
</template>

<script>
import Title from './Title.vue';

export default {
  name: 'App',
  components: {
    Title,
  },
  data() {
    return {
      hello: 'WORLD',
      count: 0,
      shouldAppear: true,
    };
  },
};
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
}
</style>
