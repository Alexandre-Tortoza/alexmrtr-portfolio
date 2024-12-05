<template>
  <main>
    <SepareatorComponent :starPosition="0.8" />
    <div class="container_width">
      <HeroComponent />
    </div>
    <SepareatorComponent :starPosition="0.35" />
    <div class="container_width">
      <AboutComponent />
    </div>
    <div style="background-color: #f6f7f7">
      <ExperienceComponent />
    </div>
    <SepareatorComponent :starPosition="0.66" />
    <div class="container_width">
      <BackgroundComponent />
    </div>
  </main>
</template>

<script setup>
import SepareatorComponent from '@/components/SepareatorComponent.vue'

import HeroComponent from '@/components/HeroComponent.vue'
import AboutComponent from '@/components/AboutComponent.vue'
import ExperienceComponent from '@/components/ExperienceComponent.vue'
import BackgroundComponent from '@/components/BackgroundComponent.vue'
</script>

<style scoped></style>
