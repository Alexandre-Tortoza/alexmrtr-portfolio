<template>
  <HeaderComponent />
  <RouterView />
  <FooterComponent />
</template>

<script setup>
import { RouterView } from 'vue-router'
import HeaderComponent from '@/components/layout/HeaderComponent.vue'
import FooterComponent from './components/layout/FooterComponent.vue'
</script>
