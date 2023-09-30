<template>
  <div class="formulario">
    <label for="nome">Nome</label>
    <input type="text" id="nome" v-model="medicamento" />

    <label for="laboratorio">Laboratório</label>
    <input type="text" id="laboratorio" v-model="laboratorio" />

    <label for="preco">Preço</label>
    <input type="number" id="preco" v-model="preco" />

    <button @click="$emit('cadastrar', medicamento, laboratorio, preco)">
      Cadastrar
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      medicamento: "",
      laboratorio: "",
      preco: 0,
    };
  },
};
</script>

<style>
.formulario {
  display: flex;
  width: 840px;
  height: 40px;
  margin: auto;
  gap: 8px;
  font-family: Arial, Helvetica, sans-serif;
  background-color: brown;
  padding: 10px;
  border-radius: 4px;
  color: white;
  font-weight: bold;
}

.formulario input {
  border: none;
  border-radius: 4px;
  padding: 3px;
}

.formulario button {
  background-color: white;
  border: none;
  border-radius: 4px;
  font-family: Arial, Helvetica, sans-serif;
  color: black;
  font-weight: bold;
  padding: 4px;
}
</style>
