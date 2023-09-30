<template>
  <div class="container">
    <div class="card">
      <img
        src="https://saude.abril.com.br/wp-content/uploads/2018/12/remc3a9dio01-3.jpg?quality=85&strip=info&w=1280&h=720&crop=1"
        alt="medicamento"
      />
      <div class="infos">
        <span>Nome: {{ nome }}</span>
        <span>Laboratorio: {{ laboratorio }}</span>
        <span>Preco: {{ preco }}</span>
      </div>
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
  background-color: brown;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 200px;
  height: 200px;
  padding-bottom: 20px;
  border-radius: 4px;
}

.card img {
  width: 80%;
  margin: auto;
  border-radius: 4px;
}

.infos {
  display: flex;
  width: 80%;
  flex-direction: column;
  font-weight: bold;
  color: white;
}
</style>
