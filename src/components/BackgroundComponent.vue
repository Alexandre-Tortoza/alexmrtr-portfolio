<template>
  <div class="flex lg:flex-row flex-col-reverse md:flex-row gap-8 p-8 py-16">
    <div class="flex flex-col gap-6 w-full">
      <div
        class="flex flex-col p-6 rounded-lg shadow-sm w-full lg:w-2/3"
        style="background-color: #dde2e3"
      >
        <div class="flex-col justify-between">
          <p class="text-sm mb-2">cursando bacharel</p>
          <h3 class="text-xl font-bold flex gap-4 items-center">
            <img src="@/assets/icons/book.svg" width="48" height="48" alt="Icon de Livro" />
            Ciência da Computação
          </h3>
          <p class="text-sm mt-2">2022-2026</p>
        </div>
      </div>
      <div class="outBlock">
        <h3 class="text-2xl font-bold flex gap-4 items-center">
          <img src="@/assets/icons/cursos.svg" width="25" height="25" alt="Icon de Livro" />
          Cursos
        </h3>
        <Transition>
          <ul class="mt-4 space-y-4" v-if="modalView">
            <li>- UI Design para Iniciantes</li>
            <li>- C# COMPLETO</li>
            <li>- CSS Flexbox</li>
            <li>- UI Design Avançado</li>
            <li class="verMais" @click="openModal">Ver mais...</li>
          </ul>

          <ul class="mt-4 space-y-4" v-else>
            <li>
              - UI Design para Iniciantes -
              <a href="https://www.origamid.com/certificate/e1ddf0d4" target="_blank">origamid</a>
            </li>
            <li>
              - C# COMPLETO -
              <a
                href="https://www.udemy.com/certificate/UC-8ef2b1f2-0715-41dc-876c-854b5f1a290f/"
                target="_blank"
              >
                Udemy</a
              >
            </li>

            <li>
              - CSS Flexbox -
              <a href="https://www.origamid.com/certificate/39f6ec3c" target="_blank"> Origamid</a>
            </li>
            <li>
              - UI Design Avançado -
              <a href="https://www.origamid.com/certificate/a453dddd" target="_blank"> Origamid</a>
            </li>
            <li>
              - Linguagem JavaScript -
              <a
                href="https://www.estudonauta.com/certificates/certificado-40h/?course_id=46447&cert-nonce=6c9d88087e"
                target="_blank"
              >
                Estudonauta</a
              >
            </li>
            <li>
              - React: ciclo de vida dos componentes -
              <a
                href="https://cursos.alura.com.br/user/a-marquestortoza/course/react-ciclo-de-vida/certificate"
                target="_blank"
              >
                Alura</a
              >
            </li>
            <li>
              - Layouts Responsivos: trabalhando com layouts mobile -
              <a
                href="https://cursos.alura.com.br/user/a-marquestortoza/course/mobile-first-layouts-responsivos/certificate"
                target="_blank"
              >
                Alura</a
              >
            </li>
            <li>
              - JavaScript: programando a Orientação a Objetos -
              <a
                href="https://cursos.alura.com.br/user/a-marquestortoza/course/javascritpt-orientacao-objetos/certificate"
                target="_blank"
              >
                Alura</a
              >
            </li>

            <li>
              - JavaScript: programando na linguagem da web -
              <a
                href="https://cursos.alura.com.br/user/a-marquestortoza/course/javascript-programando-na-linguagem-web/certificate"
                target="_blank"
              >
                Alura</a
              >
            </li>
            <li>
              - JavaScript: interfaces e Herança em Orientação a Objetos -
              <a
                href="https://cursos.alura.com.br/user/a-marquestortoza/course/javascript-polimorfismo/certificate"
                target="_blank"
              >
                Alura</a
              >
            </li>
            <li>
              - React: entendendo como a biblioteca funciona -
              <a
                href="https://cursos.alura.com.br/user/a-marquestortoza/course/react-js/certificate"
                target="_blank"
              >
                Alura</a
              >
            </li>
            <li>
              - React: Hooks, Contextos e boas práticas -
              <a
                href="https://cursos.alura.com.br/user/a-marquestortoza/course/react-hooks-e-formularios/certificate"
                target="_blank"
              >
                Alura</a
              >
            </li>
            <li>
              - React: Function Components, uma abordagem moderna -
              <a
                href="https://cursos.alura.com.br/user/a-marquestortoza/course/react-function-components/certificate"
                target="_blank"
              >
                Alura</a
              >
            </li>
            <li>
              - Sass e Compass: Descomplicando o CSS -
              <a
                href="https://cursos.alura.com.br/user/a-marquestortoza/course/sass/certificate"
                target="_blank"
              >
                Alura</a
              >
            </li>
            <li>
              - Arquitetura CSS: descomplicando os problemas -
              <a
                href="https://cursos.alura.com.br/user/a-marquestortoza/course/arquitetura-css/certificate"
                target="_blank"
              >
                Alura</a
              >
            </li>
            <li>
              - PHP: conceitos, lidando com dados, loops e mais -
              <a
                href="https://cursos.alura.com.br/user/a-marquestortoza/course/php-primeiros-passos/certificate"
                target="_blank"
              >
                Alura</a
              >
            </li>
            <li>
              - JavaScript na Web: validação de Formulários e HTML5 -
              <a
                href="https://cursos.alura.com.br/user/a-marquestortoza/course/javascript-web-validacao-formularios-html5/certificate"
                target="_blank"
              >
                Alura</a
              >
            </li>
            <li>
              - Expressões regulares: capturando textos de forma mágica -
              <a
                href="https://cursos.alura.com.br/user/a-marquestortoza/course/expressoes-regulares/certificate"
                target="_blank"
              >
                Alura</a
              >
            </li>

            <li class="verMais" @click="openModal">Ver Menos...</li>
          </ul>
        </Transition>
      </div>
      <div class="outBlock mt-4">
        <h3 class="text-2xl font-bold flex gap-4 items-center">
          <img src="@/assets/icons/cursos.svg" width="25" height="25" alt="Icon de Livro" />
          Idiomas
        </h3>
        <ul class="mt-4 space-y-4">
          <li>Português <span> - Nativo</span></li>
          <li>Inglês <span>- Intermediário</span></li>
        </ul>
      </div>
    </div>
    <div class="text-4xl md:text-6xl uppercase leading-tight">
      <h2>
        FORMA
        <br />ÇÃO
      </h2>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

let modalView = ref(true)

const openModal = () => {
  modalView.value = !modalView.value
}
</script>

<style scoped>
h2 {
  color: #03262e;
}
h3,
span,
p,
small {
  color: #000708;
}
h3,
span,
small {
  color: #000708;
}
P {
  color: #042529;
}

.outBlock h3,
.outBlock p {
  color: #f6f7f7;
}
.outBlock li > span {
  color: #526666;
  transition: all 0.6s ease-out;
}

.verMais:hover {
  text-decoration: underline;
  text-underline-offset: 5px;
  text-decoration-color: #2b7b8c;
}

li > a {
  color: #526666;
}
li > a:hover {
  color: #526666;
  text-decoration: underline;
  text-underline-offset: 5px;
  text-decoration-color: #526666;
}
</style>
