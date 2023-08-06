<template>
  <div>
    <Header />
    <FormularioNovoMedicamento @cadastrar="cadastrarMedicamento" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import FormularioNovoMedicamento from "./components/FormularioNovoMedicamento.vue";

export default {
  components: {
    Header,
    FormularioNovoMedicamento,
  },
  methods: {
    cadastrarMedicamento() {
      console.log("clicou");
    },
  },
};
</script>

<style></style>
