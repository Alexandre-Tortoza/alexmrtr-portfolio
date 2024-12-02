<template>
  <header class="flex justify-between align-middle content-center items-center py-8">
    <img src="@/assets/logo/logo_alexmrtr.svg" alt="" />
    <nav>
      <ul class="flex gap-5">
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
</style>
