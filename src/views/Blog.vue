<template>
  <div class="blog">
    <a 
      v-for="(post, idx) in posts"
      :key="idx"
      :href="post.href"
      class="post"
      target="_blank">
      <h2>
        {{post.title}}
      </h2>
      <img :src="post.src" :alt="post.title"/>
      <p>{{post.text}}</p>
    </a>
  </div>
</template>

<script>
export default {
  name: 'blog',
  data () {
    return {
      posts: [
        {
          title: 'Multiple Vue projects on GitHub Pages',
          href: 'https://medium.com/@splincool/multiple-vue-projects-on-github-pages-4aaca392f350',
          src: 'https://cdn-images-1.medium.com/max/800/1*tKPihnpnGLEbVmIUBkMkQA.png',
          text: 'I am going to share my experience with hosting Vue projects on Github pages but it should work with your host platform as well...'
        }
      ]
    }
  }
}
</script>

<style>
.blog {
  max-width: 1050px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.post {
  max-width: 500px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  text-decoration: none;
  padding: 1.5rem;
  background: #fff;
  border: 1px solid #ebecec;
  border-radius: 6px;
  -webkit-box-shadow: 0 1px 2px rgba(0,0,0,.1);
  box-shadow: 0 1px 2px rgba(0,0,0,.1);
}

.post:visited {
  color: #000;
}

.post img {
  width: 85%;
}

.post h2,
.post p {
  text-align: center;
}

@media only screen and (max-width: 370px) {
  .cool-link {
    margin-right: 10px;
  }
}
</style>
