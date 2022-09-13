<template>
  <div>
    <p>
      Login <br> 
      <input type="text">
    </p>
    <p>
      Password <br> 
      <input type="password">
    </p>
    <input type="checkbox" id="toggle">Show Password 
  </div>
</template>

<script>

export default {
  name: 'Login',
  data() {
    return {

    }
  },
}
</script>

<style>
  input {
    background:rgb(238, 238, 238);
    width: 150px;
    height: 15px;
    margin: 5px;
    padding: 2px;
    border-radius: 5px;
    border: 1px solid black;
  }

  #toggle {
    margin: 0;
    padding: 0;
  }
</style>