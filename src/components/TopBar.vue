<template>
  <header class="top-bar">
    <nav>
      <router-link
        v-for="(link, idx) in links"
        :key="idx"
        class="cool-link" 
        :to="link.to" 
        exact>
          {{link.label}}
      </router-link>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'top-bar',
  data () {
    return {
      links: [
        {
          label: 'About',
          to: '/'
        },
        {
          label: 'Skills',
          to: '/skills'
        },
        {
          label: 'Projects',
          to: '/projects'
        },
        {
          label: 'Blog',
          to: '/blog'
        },
        {
          label: 'Contact',
          to: '/contact'
        }
      ]
    }
  }
}
</script>

<style>
.top-bar {
  margin: 10px 0px 50px 0px;
}

.cool-link {
  display: inline-block;
  color: #000;
  text-decoration: none;
  margin-right: 20px;
}
.cool-link::after {
  content: '';
  display: block;
  width: 0;
  height: 2px;
  background: #000;
  transition: width .3s;
  margin-top: 5px;
}

.cool-link.router-link-exact-active::after {
  content: '';
  display: block;
  width: 100%;
  height: 2px;
  background: #000;
}

</style>
