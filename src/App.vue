<!--Monday 6/13:
Navbar red bg white/pale green text?
-->
<template>
  <!DOCTYPE html>
  <html lang="en-us">
    <head>

    </head>
    <body>
      <NavBar />
      <component :is="currentView" />
    </body>
  </html>
</template>

<script>
import NavBar from './components/NavBar.vue'
import HomePage from './components/homepage/HomePage.vue'
import NotFound from './components/notfound/NotFound.vue'

const routes = {
  '/': HomePage,
}

export default {
  data() {
    return {
      currentPath: window.location.hash
    }
  },
  computed: {
    currentView() {
      return routes[this.currentPath.slice(1) || '/'] || NotFound
    }
  },
  mounted() {
    window.addEventListener('hashchange', () => {
      this.currentPath = window.location.hash
    })
  },
  name: 'App',
  components: {
    NavBar,
  }
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

</style>

