<template>
  <div class="dark:text-white">
    <Navbar />
    <Nuxt class="pt-3  px-3"/>
    <Footer/>
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
