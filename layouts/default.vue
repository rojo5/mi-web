<template>
  <div class="dark:bg-black">
    <Navbar />
    <Nuxt />
  </div>
</template>

<script>
import Navbar from '~/components/common/Navbar.vue'
//import Footer from '~/components/Sections/Footer'
export default {
  components: {
    Navbar
  }
}
</script>

<style>
</style>
