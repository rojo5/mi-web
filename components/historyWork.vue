<template>
  <div class="container px-5 py-10 mx-auto flex flex-wrap">
    <div class="flex flex-wrap w-full">
      <div class="lg:w-1/2 md:w-full md:pr-10 md:py-6">
        <div class="flex relative pb-12" v-for="(work, index) in works" :key="index">
          <div class="h-full w-11 inset-0 absolute flex items-center justify-center" v-if="index != Object.keys(works).length -1">
            <div class="w-1 bg-gray-200 pointer-events-none" :class="isPresent(index)"></div>
          </div>
          <div class="flex-shrink-0 w-11 h-11 rounded-full bg-red-400 inline-flex items-center justify-center text-white relative z-10">
            <span class="font-semibold">{{work.year}}</span>
          </div>
          <div class="flex-grow pl-4">
            <h2 class="font-medium text-lg mb-1 tracking-wider">{{work.company}} - {{work.month}}</h2>
            <p class="leading-relaxed">
              {{work.description}}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HistoryWork",
  props:{
      works: {
          type: Array,
          require: true
      }
  }, 
  methods: {
      isPresent(index) {
            return index == 0 ? 'present' : 'h-full'
      }
  }
};
</script>

<style scoped lang="css">
 .present {
     height: 120%;
 }
</style>