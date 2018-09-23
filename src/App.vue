<template>
  <div id="app">
    <TopBar/>
    <div>
      <transition name="show" mode="out-in" tag="div">
        <router-view/>
      </transition>
    </div>
  </div>
</template>

<script>
import TopBar from '@/components/TopBar.vue'
export default {
  name: 'app',
  components: {
    TopBar
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Open+Sans:400,700&subset=cyrillic,cyrillic-ext');

#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-family: 'Open Sans', sans-serif;
  padding: 10px;
}

.show-enter-active, .show-leave-active {
  -webkit-transition: 0.3s;
  transition: 0.3s;
}

.show-enter {
  -webkit-transform: translateX(-100px);
  transform: translateX(-100px);
  opacity: 0;
}

.show-leave-to {
  -webkit-transform: translateX(100px);
  transform: translateX(100px);
  opacity: 0;
}
</style>
