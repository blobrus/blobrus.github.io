<!--Thurs 6/16:
Implement Links/Contact Page. Will probably need to figure out how to make it take whole screen. If extra time style not found page similarly.
-->
<template>
  <!DOCTYPE html>
  <html lang="en-us">
    <head>
    </head>
    <body>
      <NavBar />
      <div class="pt-5">
        <component :is="currentView" />
      </div>
      <FooterBar />
    </body>
  </html>
</template>

<script>
import NavBar from './components/NavBar.vue'
import FooterBar from './components/FooterBar.vue'
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
    FooterBar,
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

p, h3 {
  text-shadow: 1px 0 0 #000, 0 -1px 0 #000, 0 1px 0 #000, -1px 0 0 #000;
}

</style>

