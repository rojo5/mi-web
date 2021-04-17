<template>
  <div>
    <IconDark v-if="$colorMode.preference != 'dark'" @click="changeTheme('dark')" class="h-5 w-5"/>
    <IconLight v-else @click="changeTheme('light')" class="h-5 w-5"/>
  </div>
</template>

<script>
export default {
  name: "ColorSwitch",
  components: {
    IconDark: () => import("@/assets/icons/dark.svg?inline"),
    IconLight: () => import("@/assets/icons/light.svg?inline"),
  },
  methods: {
      changeTheme(theme){
          this.$colorMode.preference = theme;
      }
  }
};
</script>

<style>
</style>