<template>
  <div class="container">
    <div>
      <logo />
      <h1>All Posts</h1>
      <ul>
        <li v-for="blog in blogPosts" :key="blog">{{ blog }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    };
  },
  components: {
    Logo
  },
  computed: {
    blogPosts() {
      return this.$store.state.blogPosts;
    },
  },
}
</script>

<style>

</style>
