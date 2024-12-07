<template>
  <div
    class="flex lg:flex-row flex-col-reverse justify-between align-middle items-center my-28 fade-in"
    ref="heroSection"
  >
    <div>
      <h1 class="lg:text-7xl text-4xl py-4 mt-4 lg:mt-0">
        <strong> Desenvolvedor </strong> &
        <br />
        UX/UI <strong> Designer</strong>
      </h1>
      <ul class="mt-8 flex gap-8">
        <li class="sub_links">
          <img src="@/assets/icons/linkedin.svg" alt="Linkedin " width="40" />
        </li>
        <li class="sub_links">
          <img src="@/assets/icons/github.svg" alt="Github" width="40" />
        </li>
      </ul>
    </div>

    <img :src="photo" alt="Foto Alexandre Marques" width="265" />
  </div>
</template>

<script setup>
import photo from '@/assets/images/alexmrtr_photo.png'
import { ref, onMounted } from 'vue'

const heroSection = ref(null)

onMounted(() => {
  setTimeout(() => {
    heroSection.value.classList.add('aos-active')
  }, 250)
})
</script>

<style scoped>
h1 {
  font-weight: 500;
  background: linear-gradient(
    45deg,
    hsl(190, 56%, 40%),
    hsl(190, 68%, 62%),
    hsl(195, 81%, 27%),
    hsl(195, 61%, 55%)
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;

  -webkit-animation: glow 1s ease-in-out infinite alternate;
  -moz-animation: glow 1s ease-in-out infinite alternate;
  animation: glow 6s ease-in-out infinite alternate;
}

@keyframes glow {
  from {
    text-shadow: 0 0 10px #3f95a80c;
  }
  to {
    text-shadow: 0 0 15px #3f95a827;
  }
}

h1 strong {
  font-weight: 700;
}
.sub_links img {
  transition: 1s;
  filter: brightness(70%);
}
.fade-in img {
  transition: 1s;
}
.fade-in img:hover {
  transform: scale(105%);
}
.sub_links img:hover {
  filter: brightness(100%);
  transform: scale(110%);
}
</style>
