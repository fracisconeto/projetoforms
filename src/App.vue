<script setup>
import { reactive, ref } from 'vue'

const titulo = ref('ola seus putos')

const produto = reactive({
  nome: '',
  preco: 0,
  quantidade: 0,
  categorias: []
})
const mostrarResultado = false
</script>

<template>
  <div class="putos">
    <h1>{{ titulo }}</h1>
  </div>
  <div class="container">
    <div class="forms">
      <h2>formulários</h2>
      <input type="text" v-model="titulo" />
      <div>
        <div class="row">
          <label for="nome">nome:</label>

          <input type="text" v-model="produto.nome" />
        </div>
      </div>
      <div>
        <div class="row">
          <label for="preco">preço:</label>
          <input type="text" v-model="produto.preco"/>
        </div>
      </div>
      <div>
        <div class="row">
          <label for="quantidade = ">quantidade:</label>

          <input type="text" v-model="produto.quantidade"/>
        
        </div>
        <div class="row">
          <label for="categoria">categoria</label>
          <input type="text" v-model="produto.categorias">
        </div>
        <button @click="mostrarResultado = !mostrarResultado">mostra</button>
      </div>
    </div>

    <div class="resultado">
      <h2>dados do produto</h2>
      <p>nome: {{ produto.nome }}</p>
      <p>preço:{{ produto.preco }}</p>
      <p>quantidade:{{ produto.quantidade }}</p>
      <p>categorias:{{ produto.categorias }}</p>
      <p>{{ mostrarResultado }}</p>
    </div>
  </div>
</template>

<style scoped>
.putos {
  text-align: center;
  margin: 10px;
  background-color: white;
  color: black;
}
.container {
  display: flex;
  gap: 2rem;
  justify-content: center;
  margin-top: 1rem;
}

.forms {
  background-color: brown;
  color: white;
  width: 45vw;
  min-height: 70vh;
  border-radius: 20px;
  padding: 20px;
}

.resultado {
  background-color: black;
  color: white;
  width: 45vw;
  min-height: 70vh;
  border-radius: 20px;
  padding: 20px;
}

.row{
  margin: 5px;
}
</style>
