<!--Tues 6/14:
Fix black outline to be sitewide. Finish my skills (c#, java, python, js/html/css, vue, react). Figure out how to to pages without py at start?
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
import MySkills from './components/skills/MySkills.vue'

const routes = {
  '/': HomePage,
  'skills': MySkills,
}

export default {
  data() {
    return {
      currentPath: window.location.hash
    }
  },
  computed: {
    currentView() {
      console.log(this.currentPath.slice(1))
      return routes[this.currentPath.slice(1) || '/'] || NotFound
    }
  },
  mounted() {
    let faScript = document.createElement('script')
    faScript.setAttribute('src', "https://kit.fontawesome.com/044156b56d.js")
    faScript.setAttribute('crossorigin', "anonymous")
    document.head.appendChild(faScript)
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

