<template>
  <div>
    <label for="nome">Nome</label>
    <input type="text" id="nome" v-model="medicamento" />

    <label for="laboratorio">Laboratório</label>
    <input type="text" id="laboratorio" v-model="laboratorio" />

    <label for="preco">Preço</label>
    <input type="number" id="preco" v-model="preco" />

    <button @click="$emit('cadastrar')">Cadastrar</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      medicamento: "",
      laboratorio: "",
      preco: 1,
    };
  },
};
</script>

<style></style>
