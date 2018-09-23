<template>
  <div class="skills">
    <div class="card">
      <img src="@/assets/vue.png" alt='vue'/>
      <h3>Vue.js</h3>
    </div>
    <div class="card">
      <img src="@/assets/nuxt.jpg" alt='nuxt'/>
      <h3>Nuxt.js</h3>
    </div>
    <div class="card">
      <img src="@/assets/js.png" alt='js'/>
      <h3>JavaScript</h3>
    </div>
    <div class="card">
      <img src="@/assets/html5.png" alt='html5'/>
      <h3>HTML</h3>
    </div>
    <div class="card">
      <img src="@/assets/css3.png" alt='css'/>
      <h3>CSS</h3>
    </div>
    <div class="card">
      <img src="@/assets/sass.png" alt='sass'/>
      <h3>Sass</h3>
    </div>
    <div class="card">
      <img src="@/assets/git.png" alt='git'/>
      <h3>Git</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: 'skills',
  data () {
    return {
    }
  }
}
</script>

<style>
.skills {
  max-width: 1050px;
  display: flex;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}

.card {
  min-width: 150px;
  -webkit-transition: all 200ms ease;
  transition: all 200ms ease;
  padding: 2.5rem;
  background: #fff;
  border: 1px solid #ebecec;
  border-radius: 6px;
  -webkit-box-shadow: 0 1px 2px rgba(0,0,0,.1);
  box-shadow: 0 1px 2px rgba(0,0,0,.1);
  margin: .5rem
}

.card:hover {
  -webkit-transform: translateY(-1px);
  transform: translateY(-1px);
  -webkit-box-shadow: 0 6px 25px rgba(0,0,0,.1);
  box-shadow: 0 6px 25px rgba(0,0,0,.1)
}

.card img {
  display: block;
  margin: 0 auto;
  max-width: 50px;
  border-radius: 6px
}

.card h3 {
  font-weight: 400;
  font-size: 1rem;
  margin: 2rem 0 0;
  text-align: center
}

</style>