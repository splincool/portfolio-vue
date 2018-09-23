<template>
  <div class="about">
    <div class="avatar"></div>
    <div class="text-about">
      <p>Hello, I am Max</p>
      <p>
        I specialize in front-end development and I will convert your brilliant design into quality and bulletproof HTML/CSS/Javascript!
      </p>
      <p>
        I am very passion Vue.js developer and I have been working with this framework for a year. 
        It is very interesting for me to learn new things regarding Vue and then implement all those features in SPA applications.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'about'
}
</script>

<style>
.about {
  max-width: 1050px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.avatar {
  background: url('../assets/ava.jpg');
  width: 150px;
  height: 150px;
  border-radius: 100%;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
.text-about {
  text-align: center;
}
</style>
