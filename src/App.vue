<template>
  <div class="container">
    <div class="navbar">
      <Navbar />
    </div>
  </div>
  <router-view/>
    <div class="footer">
    <Footer />
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
}
.navbar {
  padding: 10px;
  font-weight: bold;
  text-align: center;
  margin-bottom: 10px;
}

</style>
