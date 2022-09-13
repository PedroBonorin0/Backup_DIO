<template>
  <div>
    <h1>Custom input</h1>
    <input type="text" @input="$emit('input', $event.target.value)" :value="value" />
  </div>
</template>

<script>
export default {
  name: 'Input',
  props: ['value']
}
</script>

<style>
  input {
    width: 250px;
    height: 24px;
    border: 1 solid rgb(240, 235, 241);
    background-color: rgb(234, 227, 238);
    border-radius: 5px;
  }
</style>