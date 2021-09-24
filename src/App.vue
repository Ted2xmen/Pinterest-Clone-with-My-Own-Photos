<template>
  <div id="nav">
    <!-- <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> -->
          <Navbar />

  </div>
  <router-view/>
</template>



<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
background-color: #090909;
opacity: 1;
background-image: radial-gradient(#06e804 0.55px, #090909 0.55px);
background-size: 11px 11px;
}


</style>


<script>
import Navbar from './components/Navbar.vue'
export default {
  name: 'App',
  components: {
    Navbar
  }

}
</script>