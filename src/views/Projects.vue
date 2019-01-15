<template>
  <div class="projects">
    <a v-for="(project, idx) in projects"
      :key="idx"
      :href="project.href" 
      class="project"
      target="_blank">
      <img :src="project.src" :alt="project.title"/>
      <h3>{{project.title}}</h3>
    </a>
  </div>
</template>

<script>
export default {
  name: 'projects',
  data () {
    return {
      projects: [
        {
          title: 'Twitch Vue app',
          href: 'projects/twitch/index.html',
          src: require('../assets/twitch.png')
        },
        {
          title: 'Movies Vue app',
          href: 'projects/movie-network/index.html',
          src: require('../assets/movies.png')
        },
        // {
        //   title: 'Memory cards Vue app',
        //   href: 'projects/memory-cards/index.html',
        //   src: require('../assets/memory-cards.png')
        // },
        {
          title: 'Corporate landing page',
          href: 'projects/corporate-landing-page/index.html',
          src: require('../assets/corporate-landing-page.png')
        },
        {
          title: 'Birds game',
          href: 'projects/birds-game/index.html',
          src: require('../assets/birds-game.png')
        }
      ]
    }
  }
}
</script>

<style>
.projects {
  max-width: 1050px;
	margin: 0 auto;
	display: grid;
	grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
	grid-gap: 10px
}

.project {
  display: flex;
  flex-direction: column;
  width: auto;
  text-decoration: none;
  position: relative;
  overflow: hidden;
  cursor: pointer;
  color: #000;
}

.project:before{
	position: absolute;
	z-index: -1;
	top: 0;
	left: 0;
	bottom: 0;
	right: 0;
	content: "";
	background: #fff000;
	transition: transform 0.3s ease-in-out;
	transform: translate(0,-101%);
}

.project:hover:before{
	transform: translate(0,0);
	transition: transform 0.3s ease-in-out;
}

.project:visited {
  color: #000;
}

.project img {
  display: block;
  width: 100%;
}

.project h3 {
  margin-top: 0px;
  padding: 0 20px 10px 20px;
  font-weight: 400;
}
</style>
