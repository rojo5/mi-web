<template>
  <section class="md:flex">
      <article class="mb-20 w-full max-w-3xl mx-auto">
          <h1 class="text-4xl"> {{post.title}}</h1>
          <p class="opacity-50 pt-5">
              <span>🗓 {{ parseDate(post.date)}}</span>
          </p>
          <div class="divider" />
          <nuxt-content :document="post" />
      </article>
  </section>
</template>

<script>
export default {
    async asyncData({params, $content}) {
        const post = await $content(`blog/${params.slug}`).fetch();

        return {post}
    },
    head() {
        return {
            title: `${this.post.title}`
        }
    },
    methods: {
        parseDate(date){
                const months = [
                'Enero', 'Febrero', 'Marzo',
                'Abril', 'Mayo', 'Junio',
                'Julio', 'Agosto', 'Septiembre',
                'Octubre', 'Noviembre', 'Diciembre'
            ];
            console.log('Fecha: ' +date);
            const newDate = new Date(date);
            const year = newDate.getFullYear();
            const month = months[newDate.getMonth()]
            console.log('Mes: ' + month);
            return `${month}, ${year}`;
        }
    },
}
</script>

<style lang="scss" scoped>
.divider {
    @apply border-4 border-red-400 w-60 rounded mt-4 mb-8 mx-auto;
}
</style>