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

        <p class="mt-4 leading-7">
          {{ experience.content }}
        </p>
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
      'esenvolvimento da plataforma principal, garantindo uma experiência de usuário eficiente e intuitiva. Implementação de melhorias contínuas e integrações para aprimorar a funcionalidade e a performance da plataforma. Utilização de tecnologias como Vue3, .NET, Vue, SQL Server, HTML e CSS para construir soluções robustas e escaláveis.',
  },
  {
    comapnyName: 'Apoiar - Serviços Administrativos',
    period: 'mar de 2024 - jun de 2024',
    position: 'Estágio',
    stacks: ['React', 'JavaScript', 'HTML', 'CSS', 'PHP', 'Bootstrap 5', 'WordPress'],
    content:
      'Monitoramento e acompanhamento ativo do desenvolvimento de softwares e programas, garantindo aderência aos objetivos e prazos estabelecidos. Participação na identificação e resolução de falhas no sistema, colaborando com a equipe para garantir a integridade e o desempenho do software. Contribuição no processo de desenvolvimento de software, incluindo a implementação de soluções de automação, escrita de código limpo e eficiente, e realização de testes rigorosos para assegurar a qualidade do produto final.',
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
small {
  color: #000708;
}
/* p {
  color: red;
} */
</style>
