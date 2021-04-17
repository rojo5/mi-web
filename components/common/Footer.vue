<template>
  <footer class="text-gray-600 ">
      <div class="container px-5 py-8 mx-auto flex items-center sm:flex-row flex-col">
      <span class=" inline-flex sm:mt-0 mt-4 justify-center sm:justify-start text-2xl">
          <a href="#" class="hover:text-red-400"><fa :icon="['fab', 'instagram']" /></a>
          <a href="#" class="ml-3 hover:text-red-400"><fa :icon="['fab', 'github']" /></a>
          <a href="#" class="ml-3 hover:text-red-400"><fa :icon="['fab', 'twitter']" /></a>
      </span>
      <p class="text-sm text-gray-600 sm:ml-4 sm:pl-4 sm:border-l-2 sm:border-gray-200 sm:py-2 sm:mt-0 mt-4 dark:text-white">
          {{ new Date().getFullYear() }}  Hecho con amor y cariño por <a href="https://github.com/rojo5" target="_blank" class="text-gray-500 ml-1 dark:text-white">@rojo5</a>
      </p>
      <div class=" inline-flex sm:ml-auto">
          <a href="#top" class="hover:text-red-400" ><fa :icon="['fas', 'rocket']" class="transform -rotate-45" /></a>
      </div>
      </div>
  </footer>


</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style>

</style>