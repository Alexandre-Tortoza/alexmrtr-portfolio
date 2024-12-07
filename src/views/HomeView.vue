<template>
  <main>
    <SepareatorComponent :starPosition="0.8" />
    <div class="container_width">
      <HeroComponent />
    </div>

    <div class="fade-right" ref="heroSeparator">
      <SepareatorComponent :starPosition="0.35" />
    </div>

    <div class="container_width fade-up" ref="aboutSection" id="sobre">
      <AboutComponent />
    </div>

    <div style="background-color: #f6f7f7" id="experiencia">
      <div class="fade-up" ref="ExperienceSection">
        <ExperienceComponent />
      </div>
    </div>

    <SepareatorComponent :starPosition="0.66" />
    <div class="container_width fade-up" ref="backgroundSection">
      <BackgroundComponent id="formacao" />
    </div>

    <div class="container_width fade-down" ref="skillsSection">
      <SkillsComponent />
    </div>

    <div class="container_width fade-in" ref="contactSection">
      <ContactComponent id="contato" />
    </div>
  </main>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import SepareatorComponent from '@/components/SepareatorComponent.vue'
import HeroComponent from '@/components/HeroComponent.vue'
import AboutComponent from '@/components/AboutComponent.vue'
import ExperienceComponent from '@/components/ExperienceComponent.vue'
import BackgroundComponent from '@/components/BackgroundComponent.vue'
import ContactComponent from '@/components/ContactComponent.vue'
import SkillsComponent from '@/components/layout/SkillsComponent.vue'

const heroSeparator = ref(null)
const aboutSection = ref(null)
const backgroundSection = ref(null)
const skillsSection = ref(null)
const contactSection = ref(null)
const ExperienceSection = ref(null)

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting && entry.intersectionRatio >= 0.25) {
          entry.target.classList.add('aos-active')
        }
      })
    },
    {
      threshold: 0.25,
    },
  )

  if (heroSeparator.value) observer.observe(heroSeparator.value)
  if (aboutSection.value) observer.observe(aboutSection.value)
  if (backgroundSection.value) observer.observe(backgroundSection.value)
  if (skillsSection.value) observer.observe(skillsSection.value)
  if (contactSection.value) observer.observe(contactSection.value)
  if (ExperienceSection.value) observer.observe(ExperienceSection.value)
})
</script>

<style>
.fade-in {
  opacity: 0;
  transform: translateY(50px);
  transition: all 0.6s ease-out;
}
.fade-in.aos-active {
  opacity: 1;
  transform: translateY(0);
}

.fade-up {
  opacity: 0;
  transform: translateY(50px);
  transition: all 0.6s ease-out;
}
.fade-up.aos-active {
  opacity: 1;
  transform: translateY(0);
}

.fade-down {
  opacity: 0;
  transform: translateY(-50px);
  transition: all 0.6s ease-out;
}
.fade-down.aos-active {
  opacity: 1;
  transform: translateY(0);
}

.fade-left {
  opacity: 0;
  transform: translateX(-50px);
  transition: all 0.6s ease-out;
}
.fade-left.aos-active {
  opacity: 1;
  transform: translateX(0);
}

.fade-right {
  opacity: 0;
  transform: translateX(50px);
  transition: all 0.6s ease-out;
}
.fade-right.aos-active {
  opacity: 1;
  transform: translateX(0);
}
html {
  scroll-behavior: smooth;
}
</style>
