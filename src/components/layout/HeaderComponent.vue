<template>
  <header class="flex justify-between align-middle content-center items-center py-6 px-6 lg:px-0">
    <img
      class="hidden lg:block"
      src="@/assets/logo/logo_alexmrtr-alt.svg"
      alt="Alexandre Marques"
    />
    <img
      class="block lg:hidden"
      src="@/assets/logo/logoMobile_alexmrtr-alt.svg"
      alt="Alexandre Marques"
    />

    <nav>
      <ul class="gap-5 hidden lg:flex">
        <!--
         <li>
          <RouterLink to="/home">Home</RouterLink>
        </li>
        -->
        <li>
          <a href="#sobre">Sobre</a>
        </li>
        <li>
          <a href="#sobre">Exeriências</a>
        </li>
        <li>
          <a href="#sobre">Formação</a>
        </li>
        <li>
          <a href="#sobre">Contato</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script setup>
import { RouterLink } from 'vue-router'
</script>

<style scoped>
header {
  max-width: 1024px;
  margin: auto;
}
a {
  transition: color 1s cubic-bezier(0.075, 0.82, 0.165, 1);
}

a:hover {
  color: #4595a7;
}
</style>
