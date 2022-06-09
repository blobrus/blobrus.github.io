<!--Thursday 6/9:
About Me section (white with blue text?)
Add section tags or whatever for easier nav?
-->
<template>
    <NavBar />
    <MyNameIsWill />
    <!--
      <HelloWorld msg="Welcome to Your Vue.js App"/>
    -->
    <AboutMe />
    <MyProjects />
    <ContactMe />
</template>

<script>
import NavBar from './components/NavBar.vue'
import AboutMe from './components/homepage/AboutMe.vue'
import MyProjects from './components/homepage/MyProjects.vue'
import ContactMe from './components/homepage/ContactMe.vue'
import MyNameIsWill from './components/homepage/MyNameIsWill.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    AboutMe,
    MyProjects,
    ContactMe,
    MyNameIsWill
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
  margin-top: 60px;
}
</style>

