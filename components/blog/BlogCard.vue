<template>
  <div class="post" @click="selectPost">
      <h1 class="font-semibold text-2xl text-gray-500 dark:text-gray-200">{{title}}</h1>
      <div class="bottom-post">
          <span>🗓 {{parseDate(date)}}</span>
      </div>
      <p> {{description}}</p>
  </div>
</template>

<script>
export default {
    name:'Blog-card',
    props: {
        title: {
            type: String,
            required: true
        },
        description: {
            type: String,
            required: true
        },
        date: {
            type:String,
            required:true
        },
    },
    methods: {
        selectPost() {
            this.$emit('select');
        },
        parseDate(date) {
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
<style scoped lang="scss">
.post {
    transition: box-shadow 0.5s ease, transform 0.5s ease;
    padding: 10px;

    @apply flex flex-col cursor-pointer mb-4 border border-gray-300 rounded-md;
}

.post:hover {
    box-shadow: 4px 10px 20px var(--blog-card-shadow);
    transform: translate3d(0, -3px, 0);
}

.bottom-post {
 padding-top: 5px;

 @apply flex items-center;

//  & span:first-child {
//      @apply pr-4;
//  }
}

@media (max-width: 640px){
    .post:hover{
        box-shadow: unset;
    }
}
</style>