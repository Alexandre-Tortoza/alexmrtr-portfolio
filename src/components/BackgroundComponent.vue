<template>
  <div class="flex lg:flex-row flex-col-reverse md:flex-row gap-8 p-8 container_width">
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
        <ul class="mt-4 space-y-4">
          <li>- Design de interface do usuário (UI Design)</li>
          <li>- C# COMPLETO</li>
          <li>- Formação Front-end</li>
          <li>- PHP: conceitos, lidando com dados, loops e mais</li>
          <li>...</li>
        </ul>
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
}
</style>
