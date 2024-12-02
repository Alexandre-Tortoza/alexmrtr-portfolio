<template>
  <div class="line-with-star">
    <div class="line"></div>
    <img :src="star" alt="star" class="star-icon" :style="{ left: `${starPosition * 100}%` }" />
  </div>
</template>

<script setup>
import star from '@/assets/icons/star_icon.png'

// Definindo a posição da estrela via prop
const props = defineProps({
  starPosition: {
    type: Number,
    default: 0.5, // Posição padrão (meio da linha)
    validator: (value) => value >= 0 && value <= 1, // Deve estar entre 0 e 1
  },
})
</script>

<style scoped>
.line-with-star {
  position: relative;
  display: flex;
  align-items: center;
  max-width: 1024px;
  margin: auto;
  height: 3px;
  background-color: #073943;
}

.line {
  width: 100%;
  height: 3px;
  background-color: #073943;
  position: relative;
}

.star-icon {
  position: absolute;
  top: -23px;
  transform: translateX(-30%);
  width: 50px;
  height: 50px;
}
</style>
