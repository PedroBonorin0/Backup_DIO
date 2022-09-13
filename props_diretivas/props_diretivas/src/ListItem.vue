<template>
  <li @click="$emit('increment', 5, $event)">Click me!</li>
</template>

<script>
  export default {
    name: 'ListItem',
  }
</script>

<style>
  li{
    cursor: pointer;
    user-select: none;
  }
  li:hover{
    text-decoration: underline;
    color: rgb(45, 45, 156);
  }
</style>