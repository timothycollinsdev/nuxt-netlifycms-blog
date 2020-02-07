<template>
  <div>
    <div>
      <h1>All Posts</h1>
      <ul>
        <li v-for="blog in blogPosts" :key="blog.slug">
          <nuxt-link :to='blog.slug'>{{ blog.title }}</nuxt-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>


export default {
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    };
  },
  data(){
    return {
      open: false,
    }
  },
  computed: {
    blogPosts() {
      return this.$store.state.blogPosts;
    },
  },
  methods: {
  	toggle() {
    	this.open = !this.open
    }
  }
}
</script>

<style>

</style>
