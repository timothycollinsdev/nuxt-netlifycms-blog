<template>
</template>

<script>
export default {
    name: "blogpost",
    computed: {
    blogPosts() {
      return this.$store.state.blogPosts;
    },
    }
}
</script>
<style lang="css">
    
</style>