<template>
  <div class="dark:text-white  items-center">
    <section class="container pb-10 items-center md:grid grid-cols-2 md:gap-4 mx-auto px-10 sm:space-y-5">
      <div class="mb-4">
        <div class="grid grid-rows-1 grid-flow-row">
          <h1 class="text-3xl font-extrabold text-gray-600  dark:text-white">
            Luis Lorenzo
          </h1>
          <small>Software developer</small>
        </div>
        <p>
          Hola, soy Luis, soy desarrollador full stack, con más de 2 años de experiencia 
          en el mundo de consultoria informatica.
        </p>
        <p>
          Actualmente enfoco mi desarrollo para la creación de aplicaciones web, las pricipales
          tecnologias con las que trabajo son Java, Groovy, JavaScript, Vue, Nuxt...
        </p>
      </div>

      <div class="image-wrapper">
        <img  src="~/assets/images/ejemplo.jpg" class=" 2xl:h-full h80" alt="Imagen de ejemplo" />
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
          company:'Bluetab Solutions',
          description: 'Desarrollo de aplicaciones web para clientes. Tecnologias: Java, Groovy, Javascript, Vue y Nuxt',
          year: 2019,
          month:'Abril'
        },
        {
          company:'Atos IT',
          description: 'Mantenimiento y desarrollo de aplicaciones para clientes. Tecnologias Java, JavaScript, Gaia y Angular',
          year: 2018,
          month:'Junio'
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
