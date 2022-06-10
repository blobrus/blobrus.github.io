<template>
  <head>

  </head>
  <body>
    <MyNameIsWill />
    <AboutMe />
  </body>
  
</template>

<script>
import MyNameIsWill from './homecomponents/MyNameIsWill.vue'
import AboutMe from './homecomponents/AboutMe.vue'

export default {
  name: 'HomePage',
  components: {
    MyNameIsWill,
    AboutMe
  }
}
</script>

<style scoped>
body {
  background-image: url('../../assets/geo.jpg');
  height: 100%;
  background-position: center;
  background-repeat: no-repeat;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
}

.bg {
  height: 100%;
}
</style>
