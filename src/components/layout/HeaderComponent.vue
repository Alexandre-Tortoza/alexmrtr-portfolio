<template>
  <div class="header__container">
    <header
      class="flex justify-between align-middle content-center items-center py-6 px-6 lg:px-0 lg:top-0"
    >
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
        <!-- Menu desktop -->
        <ul class="gap-5 hidden lg:flex">
          <li><a href="#sobre">Sobre</a></li>
          <li><a href="#experiencia">Exeriências</a></li>
          <li><a href="#formacao">Formação</a></li>
          <li><a href="#contato">Contato</a></li>
        </ul>

        <!-- Ícone menu mobile -->
        <div @click="callMenu" class="block lg:hidden relative z-50">
          <img width="40" src="@/assets/icons/menu.svg" alt="" />
        </div>

        <!-- Menu mobile -->
        <div class="elemento fixed top-0 right-0 w-3/5 h-full pt-24" :class="menuAnimation">
          <div v-if="modalView" class="p-4">
            <ul class="flex flex-col gap-8">
              <li><a href="#sobre" @click="callMenu">Sobre</a></li>
              <li><a href="#experiencia" @click="callMenu">Experiências</a></li>
              <li><a href="#formacao" @click="callMenu">Formação</a></li>
              <li><a href="#contato" @click="callMenu">Contato</a></li>
            </ul>
          </div>
        </div>
      </nav>
    </header>
    <SepareatorComponent :starPosition="0.8" />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import SepareatorComponent from '../SepareatorComponent.vue'

const modalView = ref(false)
const menuAnimation = ref('')

const callMenu = () => {
  if (modalView.value) {
    // Fechando o menu
    menuAnimation.value = 'out'
    setTimeout(() => {
      modalView.value = false
    }, 500)
  } else {
    // Abrindo o menu
    modalView.value = true
    menuAnimation.value = 'in'
  }
}
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

/* Animações do menu mobile */
.elemento {
  transform: translateX(100%);
  transition: transform 0.5s ease-in-out;
  background-color: #030405fa;
  z-index: 10;
}

.elemento.in {
  transform: translateX(0);
}
.elemento.out {
  transform: translateX(100%);
}
@media (max-width: 1024px) {
  .header__container {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    backdrop-filter: blur(10px);
    background: #08090df3;
    z-index: 9999;
  }
}
</style>
