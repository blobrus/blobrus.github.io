<!--Tues 6/14:
Finish my skills (c#, java, python, js/html/css, vue, react).
-->
<template>
  <!DOCTYPE html>
  <html lang="en-us">
    <head>
    </head>
    <body>
      <NavBar />
      <div class="py-5">
        <component :is="currentView" />
      </div>
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
    //Font Awesome implementation
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

h1 {
  text-shadow: 2px 0 0 #000, 0 -2px 0 #000, 0 2px 0 #000, -2px 0 0 #000;
}

p {
  text-shadow: 1px 0 0 #000, 0 -1px 0 #000, 0 1px 0 #000, -1px 0 0 #000;
}

</style>

