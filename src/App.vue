<script setup>
import { reactive, ref } from 'vue'

const titulo = ref('ola seus putos')

const produto = reactive({
  nome: '',
  email: '',
  senha: '',
  categorias: []
})

   

const mostrarResultado = false
</script>

<template>
  <div class="putos"> /h1>
  </div>
  <div class="container">
    <div class="forms">
      <h2>formulários</h2>
      <input type="text" v-model="titulo" />
      <div>
        <div class="row">
          <label for="nome">nome:</label>
          <input type="text" v-model="produto.nome" />

          <label for="email">email:</label>
          <input type="email" v-model="produto.email">

          <label for="senha">senha:</label>
          <input type="password" v-model="produto.senha">

          <label for="confirma">confirmação de senha:</label>
          <input type="password" v-model="produto.confirma">

          <label for="data">data de nacimento:</label>
          <input type="date" v-model="produto.data">
              
          <label for="cidade">cidade:</label>
          <input type="text" v-model="produto.cidade">
        
          <label for="estado">estado:</label>
          <input type="select" >
        
        </div>
      </div>
    </div>

    <div class="resultado">
      <h2>dados do produto</h2>
      <p>nome: {{ produto.nome }}</p>
      <p>email:{{ produto.email }}</p>
      <p>senha:{{ produto.senha }}</p>
      <p>confirmação da senha:{{ produto.confirma }} </p>
      <p>data de nacimento:{{ produto.data }}</p>
      <p>cidade:{{produto.cidade}}</p>
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

.row {
  margin: 5px;
}
</style>
