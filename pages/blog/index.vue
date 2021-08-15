<template>
  <div class="flex flex-col m-auto pt-8 container">
      <blog-card v-for="(post, index) in posts" :key="index" v-bind="post" @select="goToPost(post.path)"/>
  </div>
</template>

<script>
import BlogCard from '~/components/blog/BlogCard.vue'
export default {
  components: { BlogCard },
  name:'Blog',
  async asyncData({$content}) {

      const posts =  await $content('blog')
      .without(['body'])
      .fetch();

      return {posts};
  },
  methods: {
    goToPost(path) {
      this.$router.push({path})
    }
  },
}
</script>

<style>

</style>