<template>
  <div class="projects">
    <a 
      target="_blank" 
      href="/twitch/index.html" 
      class="project">
      <img src="@/assets/twitch.png" alt='twitch'/>
      <h3>Twitch Vue app</h3>
    </a>
    <a 
      target="_blank" 
      href="/memory-cards/index.html" 
      class="project">
      <img src="@/assets/memory-cards.png" alt='memory-cards'/>
      <h3>Memory cards Vue app</h3>
    </a>
    <a 
      target="_blank" 
      href="/corporate-landing-page/index.html"
      class="project">
      <img 
          src="@/assets/corporate-landing-page.png" 
          alt='corporate-landing-page'/>
      <h3>Corporate landing page</h3>
    </a>
    <a       
      target="_blank" 
      href="/birds-game/index.html"
      class="project">
      <img src="@/assets/birds-game.png" alt='birds-game'/>
      <h3>Birds game</h3>
    </a>
  </div>
</template>

<script>
export default {
  name: 'projects',
  data () {
    return {

    }
  }
}
</script>

<style>
.projects {
  max-width: 1050px;
	margin: 0 auto;
	display: grid;
	grid-template-columns: 1fr 1fr 1fr;
	grid-gap: 10px
}

.project {
  display: flex;
  flex-direction: column;
  width: 360px;
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
