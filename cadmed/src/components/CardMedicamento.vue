<template>
  <div class="container">
    <div class="card">
      <button @click="$emit('favoritar', id)">favoritar</button>
      <img src="" alt="" />
      <span>nome {{ nome }}</span>
      <span>laboratorio {{ laboratorio }}</span>
      <span>preco {{ preco }}</span>
    </div>
  </div>
</template>

<script>
export default {
  props: ["nome", "laboratorio", "preco", "favorito", "id"],
};
</script>

<style scoped>
.conatiner {
  display: flex;
}
.card {
  display: flex;
  flex-direction: column;
  width: calc(100% / 4);
}
</style>
