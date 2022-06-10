<template>
    <MyNameIsWill />
    <AboutMe />
    <MyProjects />
    <ContactMe />
</template>

<script>
import AboutMe from './homecomponents/AboutMe.vue'
import MyProjects from './homecomponents/MyProjects.vue'
import ContactMe from './homecomponents/ContactMe.vue'
import MyNameIsWill from './homecomponents/MyNameIsWill.vue'

export default {
  name: 'HomePage',
  components: {
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
