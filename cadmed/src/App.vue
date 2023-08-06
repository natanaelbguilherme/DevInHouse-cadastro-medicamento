<template>
  <div>
    <Header />
    <FormularioNovoMedicamento @cadastrar="cadastrarMedicamento" />
    <CardMedicamento
      v-for="medicamento in listaMedicamentos"
      :key="medicamento.id"
      @favoritar="favoritarMedicamento"
      :nome="medicamento.nome"
      :laboratorio="medicamento.laboratorio"
      :preco="medicamento.preco"
      :id="medicamento.id"
    />
  </div>
</template>

<script>
import { v4 as uuidv4 } from "uuid";
import Header from "./components/Header.vue";
import FormularioNovoMedicamento from "./components/FormularioNovoMedicamento.vue";
import CardMedicamento from "./components/CardMedicamento.vue";

export default {
  data() {
    return {
      listaMedicamentos: [],
    };
  },
  components: {
    Header,
    FormularioNovoMedicamento,
    CardMedicamento,
  },
  methods: {
    cadastrarMedicamento(nome, laboratorio, preco) {
      if (nome == "" || laboratorio == "" || preco == 0) {
        alert("preencha todos os camos");
      } else {
        const novoMedicamento = {
          id: uuidv4(),
          nome: nome,
          laboratorio: laboratorio,
          preco: preco,
          favorito: false,
        };
        this.listaMedicamentos.push(novoMedicamento);
      }
    },
    favoritarMedicamento() {
      console.log("teste");
    },
  },
};
</script>

<style></style>
