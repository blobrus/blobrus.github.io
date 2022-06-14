<template>
  <head>

  </head>
  <body>
    <div id="skills" class="skills text-danger bg-success">
      <div class="container">
          <div class="row">
              <h1>My Skills</h1>
          </div>
          <div class="row py-3">
            <div class="col-sm-6">
              <h1 id="cSharp">C#</h1>
              <div class="text-light">
                <h3>C#</h3>
                <p>this is the body of the paragraph description</p>
              </div>
            </div>
            <div class="col-sm-6">
              <h1 id="cPlusPlus">C++</h1>
              <div class="text-light">
                <h3>C, C++</h3>
                <p>this is the body of the paragraph description</p>
              </div>
            </div>
          </div>
          <div class="row py-3">
            <div class="col-sm-6">
              <i class="fa-brands fa-java fa-5x py-2"></i>
              <div class="text-light">
                <h3>Java</h3>
                <p>this is the body of the paragraph description</p>
              </div>
            </div>
            <div class="col-sm-6">
              <i class="fa-brands fa-python fa-5x py-2"></i>
              <div class="text-light">
                <h3>Python</h3>
                <p>this is the body of the paragraph description</p>
              </div>
            </div>
          </div>
          <div class="row py-3">
            <div class="col-sm-6">
              <i class="fa-brands fa-vuejs fa-5x py-2"></i>
              <div class="text-light">
                <h3>Vue.js</h3>
                <p>this is the body of the paragraph description</p>
              </div>
            </div>
            <div class="col-sm-6">
              <i class="fa-brands fa-react fa-5x py-2"></i>
              <div class="text-light">
                <h3>React</h3>
                <p>this is the body of the paragraph description</p>
              </div>
            </div>
          </div>
          <div class="row py-3">
            <div class="col-sm-6">
              <i class="fa-solid fa-code fa-5x py-2"></i>
              <div class="text-light">
                <h3>Javascript, Html, CSS</h3>
                <p>this is the body of the paragraph description</p>
              </div>
            </div>
            <div class="col-sm-6">
              <i class="fa-solid fa-database fa-5x py-2"></i>
              <div class="text-light">
                <h3>Microsoft SQL Server</h3>
                <p>this is the body of the paragraph description</p>
              </div>
            </div>         
          </div>
      </div>
    </div> 
  </body>
</template>

<script>
export default {
  name: 'MySkills',
  components: {
  }
}
</script>

<style scoped>
h1 {
  font-size: 5rem;
}

h3{
  font-size: 2.5rem;
}

p {
  font-size: 1.3rem;
}

#cSharp, #cPlusPlus {
  text-shadow: none;
}

</style>