<template>
  <footer class="flex justify-center lg:flex-row flex-col lg:items-center py-16 px-6 lg:px-0">
    <div class="lg:w-1/2">
      <h2 class="text-4xl md:text-6xl uppercase leading-tight">Contato</h2>
      <br />
      <p class="leading-7">
        Estou disponível para novos projetos no momento. Entre em contato comigo e marcamos uma
        conversa 👋
      </p>
    </div>
    <div class="lg:w-1/2 flex lg:justify-center lg:align-middle lg:content-center lg:mt-0 mt-8">
      <ul class="flex flex-col justify-center align-middle content-center gap-2">
        <li class="flex gap-4 items-center">
          <img src="@/assets/icons/phone.svg" alt="" width="25" />
          <a href="tek:41992081308" target="_blank">(41) 99208-1308</a>
        </li>
        <li class="flex gap-4 items-center">
          <img src="@/assets/icons/mail.svg" alt="" width="25" />
          <a href="mailto:a.marquestortoza@gmail.com" target="_blank">a.marquestortoza@gmail.com</a>
        </li>
        <li class="flex gap-4 items-center">
          <img src="@/assets/icons/linkedin.svg" alt="" width="25" />
          <a href="https://www.linkedin.com/in/alexmrqr/">/alexmrtr</a>
        </li>
      </ul>
    </div>
  </footer>
</template>

<style scoped>
footer {
  max-width: 1024px;
  margin: auto;
}
a {
  transition: color 1s cubic-bezier(0.075, 0.82, 0.165, 1);
}

a:hover {
  color: #4595a7;
}
</style>
