<template>
  <div>
    <h1>
      <slot> </slot>
    </h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Nisi tempora magni hic iure.
      Recusandae non id provident repellendus ad eum. Itaque in omnis a nulla consequatur possimus
      obcaecati incidunt ullam?
    </p>
  </div>
</template>

<style scoped>
div {
  position: fixed;
  top: 0;
  right: 0;
  height: 100vh;
  width: 80vw;
  background-color: rgb(0, 0, 0);
  z-index: 9999;
}
</style>
