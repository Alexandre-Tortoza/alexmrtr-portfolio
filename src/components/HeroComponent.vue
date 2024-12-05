<template>
  <div class="flex lg:flex-row flex-col-reverse justify-between align-middle items-center my-16">
    <h1 class="lg:text-7xl text-4xl mt-4 lg:mt-0">
      Desenvolvedor
      <br />
      <strong>Front-End</strong> &
      <br />
      UX/UI <strong> Designer</strong>
    </h1>
    <img :src="photo" alt="Foto Alexandre Marques" width="265" />
  </div>
</template>

<script setup>
import photo from '@/assets/images/alexmrtr_photo.png'
</script>
<style scoped>
h1 {
  font-weight: 500;
  background: linear-gradient(
    45deg,
    hsl(190, 50%, 50%),
    /* Ajuste de saturação */ hsl(190, 70%, 60%),
    /* Aumenta saturação e luminosidade */ hsl(190, 30%, 40%) /* Reduz saturação e luminosidade */
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

h1 strong {
  font-weight: 700;
}
</style>
