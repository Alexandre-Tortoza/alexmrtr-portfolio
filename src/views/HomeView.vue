<template>
  <main>
    <!-- Hero da Pagina -->
    <SepareatorComponent :starPosition="0.8" />
    <div class="container_width">
      <HeroComponent />
    </div>
    <!-------------------->

    <!-- Sobre mim da Pagina -->
    <SepareatorComponent :starPosition="0.35" />
    <div class="container_width">
      <AboutComponent />
    </div>
    <!------------------------->

    <!-- Experiencia da Pagina -->
    <div style="background-color: #f6f7f7">
      <ExperienceComponent />
    </div>
    <!--------------------------->

    <!-- Formação da Pagina -->
    <SepareatorComponent :starPosition="0.66" />
    <div class="container_width">
      <BackgroundComponent />
    </div>
    <!-------------------------->

    <!-- Formação da Pagina -->
    <div class="container_width">
      <SkillsComponent />
    </div>
    <!-------------------------->

    <!-- Serviços da Pagina ---
    Como esse é um portfolio
    para servi como um CV
    Não vou colcoar o Serviços
    -------------------------->

    <!-- Contato da Pagina -->
    <div class="container_width">
      <ContactComponent />
    </div>
    <!----------------------->
  </main>
</template>

<script setup>
import SepareatorComponent from '@/components/SepareatorComponent.vue'

import HeroComponent from '@/components/HeroComponent.vue'
import AboutComponent from '@/components/AboutComponent.vue'
import ExperienceComponent from '@/components/ExperienceComponent.vue'
import BackgroundComponent from '@/components/BackgroundComponent.vue'
import ContactComponent from '@/components/ContactComponent.vue'
import SkillsComponent from '@/components/layout/SkillsComponent.vue'
</script>
