<template>
  <div class="flex flex-col md:flex-row gap-8 p-8 py-16 container_width">
    <div class="text-4xl md:text-6xl uppercase leading-tight">
      <h2>expe<br />riên <br />cia</h2>
    </div>

    <div class="flex flex-col gap-6 w-full">
      <div
        class="flex flex-col p-6 rounded-lg shadow-sm"
        style="background-color: #dde2e3"
        v-for="(experience, index) in experiences"
        :key="index"
      >
        <div class="items-center justify-between hidden lg:flex">
          <div>
            <h3 class="text-xl font-bold">{{ experience.comapnyName }}</h3>
            <small class="text-sm">{{ experience.period }}</small>
          </div>
          <span class="font-semibold">{{ experience.position }}</span>
        </div>
        <div class="block lg:hidden">
          <h3 class="text-xl font-bold">{{ experience.comapnyName }}</h3>
          <small class="font-medium">{{ experience.position }}</small>
          <br />
          <small class="text-sm"> {{ experience.period }}</small>
        </div>

        <p class="mt-4 leading-7">{{ experience.content }}</p>
        <ul class="my-4">
          <li v-for="(li, index) in experience.list" :key="index" class="my-2">{{ li }}</li>
        </ul>

        <div class="flex flex-wrap gap-2 mt-4">
          <span
            v-for="(stacks, index) in experience.stacks"
            :key="index"
            class="px-3 py-1 rounded"
            style="background-color: #f6f7f7"
            >{{ stacks }}</span
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const experiences = ref([
  {
    comapnyName: 'Bwise Contabilidade',
    period: 'jun de 2024 - Atualmente',
    position: 'Desenvolvedor Front-End',
    stacks: ['Vue.js', 'JavaScript', 'HTML', 'CSS', 'API', 'Bootstrap 5'],
    content:
      'Atuo no desenvolvimento do front-end das plataformas da empresa e também dos sistemas internos, realizando o design das telas, sua codificação e manutenção.',
    list: [
      'Desenvolvimento em Vue3',
      'Consumo de APIs REST full',
      'Design de Interfaces',
      'Arquitetura Limpa',
    ],
  },
  {
    comapnyName: 'Apoiar - Serviços Administrativos',
    period: 'mar de 2024 - jun de 2024',
    position: 'Estágio',
    stacks: ['React', 'JavaScript', 'HTML', 'CSS', 'PHP', 'Bootstrap 5', 'WordPress'],
    content:
      'Enquanto estágiva na apoiar nos prestavos serviço para empresas como Ennet e CPS, Trabalhei na concpção na codificação de landinpages e na manutenção dos sites em WordPress, tambem trabalhei em um sistema de ensino, criado em react, projeto em que  desenvolvi telas',
    list: [
      'Envolvimento de páginas em React',
      'Criação de landing pages',
      'Manutenção em Wordpress',
    ],
  },
])
</script>

<style scoped>
h2 {
  color: #03262e;
}
h3,
span,
p,
li,
small {
  color: #000708;
}
/* p {
  color: red;
} */

ul {
  margin-left: 1rem;
}

li {
  list-style: disc;
}
</style>
