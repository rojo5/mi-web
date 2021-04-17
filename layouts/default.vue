<template>
  <div>
    <Navbar />
    <Nuxt class="dark:bg-gray-800 dark:text-white"/>
    <Footer class="dark:bg-gray-800 dark:text-white" />
  </div>
</template>

<script>
import Footer from '~/components/common/Footer.vue'
import Navbar from '~/components/common/Navbar.vue'
export default {
  components: {
    Navbar,
    Footer
  }
}
</script>

<style>
</style>
