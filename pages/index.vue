<template>
  <div class="dark:text-white  items-center">
    <section class="pb-10 items-center md:grid grid-cols-2 md:gap-4 mx-auto px-10 sm:space-y-5">
      <div class="mb-4">
        <h1 class="text-2xl font-semibold text-gray-600 dark:text-white">
          Luis Lorenzo
        </h1>

        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe
          consectetur est sint numquam excepturi eligendi cupiditate nam,
          accusantium mollitia aspernatur inventore culpa quibusdam iusto
          voluptate error voluptates aliquid dolores sit?
        </p>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe
          consectetur est sint numquam excepturi eligendi cupiditate nam,
          accusantium mollitia aspernatur inventore culpa quibusdam iusto
          voluptate error voluptates aliquid dolores sit?
        </p>
      </div>

      <div class="image-wrapper sm:pt-4">
        <img  src="~/assets/images/example.gif" alt="Imagen de ejemplo" />
      </div>
    </section>

    <section class="mt-8">
      <h1 class="text-3xl font-semibold text-gray-600 dark:text-white text-center">Experiencia laboral 👨🏻‍💻</h1>
      <HistoryWork :works="works"/>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      works: [
        {
          company:'Empresa 1',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe consectetur est',
          year: 2019,
          month:'Abril'
        },
        {
          company:'Empresa 2',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe consectetur est',
          year: 2018,
          month:'Enero'
        },
        {
          company:'Empresa 3',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe consectetur est',
          year:'2017',
          month: 'Octubre'
        }
      ]
    }
  },
}
</script>

<style scoped lang="scss">
p {
  margin-top: 2em;
}

.image-wrapper {
  @apply rounded flex justify-center;

  img {
      @apply rounded;
  }
}
</style>
