<template>
  <div id="info" class="info bg-primary text-light">
    <div class="container">
      <div class="row align-items-center py-5">
        <div class="col-sm-6">
          <div class="row">
            <h1>Hello, I'm Will.</h1>
          </div>
          <div class="row">
            <p>A Computer Science student at Southern Illinois University Edwardsville.</p>
          </div>
          <div class="row justify-content-center py-1">
            <div class="col-sm-4">
                     <a target="_blank" href="https://docs.google.com/document/d/1y7x-9CpWVAiUM7GsNYiOnCqw12RmKRYsXAkHONHUiuA/edit?usp=sharing" class="btn btn-light" role="button">Resume</a>
            </div>     
          </div>
          <div class="row justify-content-center py-1">
            <div class="col-sm-4">
              <a href="#contact" class="btn btn-light" role="button">Contact Me</a>
            </div>
          </div>
        </div>
        <div class="col-sm-6">
            <img src="../../../assets/Attonfull.jpg" alt="Selfie" class="img-thumbnail" id="selfPicture" />
        </div>
      </div>  
    </div>         
  </div>
</template>

<script>
export default {
  name: 'MyNameIsWill',
  components: {
  }
}
</script>

<style scoped>
  #selfPicture {
    height: 300px;
    width: 200px;
  }
</style>