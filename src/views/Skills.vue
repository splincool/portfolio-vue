<template>
  <div class="skills">
    <div 
      v-for="(card, idx) in cards"
      :key="idx"
      class="card">
      <img :src="card.src" :alt="card.title"/>
      <h3>{{card.title}}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: 'skills',
  data () {
    return {
      cards: [
        {
          title: 'Vue.js',
          src: require('../assets/vue.png')
        },
        {
          title: 'Nuxt.js',
          src: require('../assets/nuxt.jpg')
        },
        {
          title: 'JavaScript',
          src: require('../assets/js.png')
        },
        {
          title: 'HTML',
          src: require('../assets/html5.png')
        },
        {
          title: 'Pug',
          src: require('../assets/pug.png')
        },
        {
          title: 'CSS',
          src: require('../assets/css3.png')
        },
        {
          title: 'Sass',
          src: require('../assets/sass.png')
        },
        {
          title: 'Git',
          src: require('../assets/git.png')
        },
      ]
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