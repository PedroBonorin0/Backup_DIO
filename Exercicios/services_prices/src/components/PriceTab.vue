<template>
  <div id="tabs">
    <h1>Services</h1>
      <ul>
        <li v-for="service in services" @click="ToggleActive(service)" :key="service.name" :class="{'active': service.active}">
          {{ service.name }} <span>${{ service.price }}</span>
        </li>
      </ul>
      <hr>
      <div class="total">
        Total: <span>${{ Total() }}</span>
      </div>
  </div>
</template>

<script>
export default {
  name: 'PriceTab',
  data() {
    return {
      services: [
        { name: 'Web Development', price: 300, active: true },
        { name: 'Design', price: 400, active: false },
        { name: 'Integration', price: 250, active: false },
        { name: 'Training', price: 220, active: false },
      ],
      total: 0,
    }
  },
  methods: {
    ToggleActive(service) {
      if(service.active) service.active = false;
      else service.active = true;
    },
    Total() {
      let total = 0;
      this.services.forEach(service => {
        if(service.active) total += service.price;
      });
      return total;
    }
  },
}
</script>

<style>
  #tabs {
    background: #61A1BC;
    width: 40%;
    margin: auto;
    color: whitesmoke;
  } 
  h1 {
    font-family: 'Trebuchet MS', Arial, sans-serif;
    margin: 20px;
    font-size: 4em;
    height: 1.2em;
    padding: 0.5em;
  }
  ul {
    font-weight: bold;
    font-size: 1.5em;
    list-style: none;
    position: relative;
    padding-bottom: 8px;
    margin-bottom: 5px;
  }
  li{
    background: #E35885;
    margin: 10px auto;
    max-width: 400px;
    height: 60px;
    padding: 0 50px;
    display: flex;
    flex-wrap: wrap;
    align-content: center;
    justify-content: space-between;
    cursor: pointer ;
  }
  .active {
    background: #5ec27c;
  }

  span {
    text-align: end;
  }
  hr {
    color: white;
    border: 0.2px solid white;
    width: 500px;
    margin: 10px auto;
  }
  .total {
    font-size: 2em;
    margin: 10px auto 12px;
    width: 400px;
    height: 60px;
    padding: 0 50px;
    display: flex;
    flex-wrap: wrap;
    align-content: center;
    justify-content: space-between;
  }
</style>