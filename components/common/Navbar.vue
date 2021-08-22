<template>
<header class="flex flex-wrap flex-row justify-between md:items-center md:space-x-4 bg-white py-6 px-6 relative dark:bg-gray-800" id="top">
  <nuxt-link  to="/" class="flex items-center text-red-400 dark:text-white">
    <!-- <svg class="fill-current h-8 w-8 mr-2" width="54" height="54" viewBox="0 0 54 54" xmlns="http://www.w3.org/2000/svg"><path d="M13.5 22.1c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05zM0 38.3c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05z"/></svg> -->
      <LogoIcon class="h-8 w-8 mr-2" />
    <span class="font-semibold text-xl tracking-tight">LuisLor</span>
  </nuxt-link>
<div class="block sm:hidden">
  <button @click="toggle" class="flex items-center px-3 py-2 border rounded text-teal-lighter border-teal-light hover:text-red-400 dark:text-white hover:border-red-400 dark:border-white">
  <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/></svg>
  </button>
</div>

  <nav :class="open ? 'block' :'hidden' " class="w-full flex-grow sm:flex  sm:items-center md:justify-end sm:justify-end sm:w-auto sm:space-x-4 font-semibold p-6 pt-0 md:p-0">
    <nuxt-link  to="/blog" class="block py-1 text-red-600  hover:text-red-400 dark:hover:text-white dark:text-red-300">Blog</nuxt-link>
    <color-switch class="sm:border-l-2  sm:pl-3"/> 
    <!-- <color-switch class="sm:pt-2 mt-3 md:mt-0"/> -->
  </nav>
</header>
</template>

<script>
import ColorSwitch from './ColorSwitch.vue'
export default {
    name:'Navbar',
    data() {
      return {
        open: false
      }
    },
    components: {
      ColorSwitch,
      LogoIcon: () => import("@/assets/icons/logo.svg?inline"),
    },
    methods: {
      toggle(){
        this.open = !this.open;
      }
    }
}
</script>

<style>

</style>