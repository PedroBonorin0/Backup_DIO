<template>
  <div>
    <nav :class="active" @click.prevent> 
      <a href="#" class="home" @click="makeActive('home')">Home</a>
      <a href="#" class="projects" @click="makeActive('projects')">Projects</a>
      <a href="#" class="services" @click="makeActive('services')">Services</a>
      <a href="#" class="contact" @click="makeActive('contact')">Contact</a>
    </nav>

    <p>
      The chosen tab is: <strong>{{ active }}</strong>.
    </p>
  </div>
</template>

<script>
export default {
  name: 'MenuBar',
  data() {
    return {
      active: 'home',
    }
  },
  methods: {
    makeActive(tab) {
      this.active = tab;
    }
  },
}
</script>

<style>
  a, a:visited {
    outline:none;
    color:#389dc1;
  }

  a:hover{
      text-decoration:none;
  }
  nav{
      display:inline-block;
      margin:60px auto 45px;
      background-color:#5597b4;
      box-shadow:0 1px 1px #ccc;
      border-radius:2px;
  }

  nav a{
      display:inline-block;
      padding: 18px 30px;
      color:#fff !important;
      font-weight:bold;
      font-size:16px;
      text-decoration:none !important;
      line-height:1;
      text-transform: uppercase;
      background-color:transparent;

      -webkit-transition:background-color 0.25s;
      -moz-transition:background-color 0.25s;
      transition:background-color 0.25s;
  }

  nav a:first-child{
      border-radius:2px 0 0 2px;
  }

  nav a:last-child{
      border-radius:0 2px 2px 0;
  }

  nav.home .home,
  nav.projects .projects,
  nav.services .services,
  nav.contact .contact{
      background-color:#e35885;
  }

  p{
      font-size:22px;
      font-weight:bold;
      color:#7d9098;
  }

  p strong{
      color:#ffffff;
      display:inline-block;
      padding:5px 10px;
      background-color:#c4d7e0;
      border-radius:2px;
      text-transform:uppercase;
      font-size:18px;
  }
</style>