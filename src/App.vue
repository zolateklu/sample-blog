<template>
  <div class="container" v-bind:style="$route.path === '/blogs'||$route.path === '/login' ? 'background-color: #c4c4c4;  z-index: -1;': '' ">
    <div class="navbar" v-bind:style="$route.path === '/blogs' ? 'background-color: #c4c4c4;height: 2rem;margin-bottom: -2rem;margin-top: 1rem;margin-left:0rem;' : '' ">
      <Navbar />
    </div>
    <router-view/>
    <div class="footer">
      <Footer />
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Footer
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: -1rem -1rem;
  
}
.navbar {
  padding: 10px;
  font-weight: bold;
  text-align: center;
}

</style>
