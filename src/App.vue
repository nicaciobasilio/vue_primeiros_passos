<script setup>
import { reactive } from 'vue';

  const nome = 'Nick'
  const meuObj = {
    nome: 'Nicacio',
    frutaFavorita: 'Uva'
  }

  function dizOla(nome) {
    return `${nome} diz oi`
  }

  const enderecoImagemUva = 'data:image/jpeg;base64,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'
  const enderecoImagemManga = 'https://static4.depositphotos.com/1020804/365/i/600/depositphotos_3653163-stock-photo-mango-with-section-on-a.jpg'

  const botaoEstaDesabilitado = false

  const gostaDeUva = true
  const gostaDeManga = false

  const estaAutorizado = false

  // let contador = 0

  const estado = reactive({
    contador: 0,
    email: '',
    saldo: 5000,
    transferindo: 0,
    nomes: ['Gian', 'Paulo', 'Nicacio', 'Alessandra'],
    nomeAInserir: ''
  })

  function incrementar() {
    estado.contador++;
  }

  function decrementar() {
    estado.contador--;
  }

  function alteraEmail(evento) {
    estado.email = evento.target.value;
  }

  function mostraSaldoFuturo() {
    const { saldo, transferindo } = estado;
    return saldo - transferindo;
  }

  function validaValorDeTransferencia() {
    const { saldo, transferindo } = estado;
    return saldo >= transferindo;
  }

  function cadastraValue() {
    if(estado.nomeAInserir.length >= 3){
      estado.nomes.push(estado.nomeAInserir)
    } else {
      alert("Digite um nome maior")
    }
  }
</script>

<template>
  <h1>{{ dizOla('Paula') }}</h1>
  <img v-if="gostaDeUva" :src="enderecoImagemUva" alt="Uva">
  <img v-else-if="gostaDeManga" :src="enderecoImagemManga" alt="Manga">
  <h2 v-else>Não curte frutas</h2>

  <h1 v-if="estaAutorizado">Bem vindo!</h1>
  <h1 v-else>Não possuí acesso</h1>

  <button :disabled="!botaoEstaHabilitado">Enviar mensagem</button>
  <br><hr>

  {{ estado.contador }}
  <button @click="incrementar" type="button">+</button>
  <button @click="decrementar" type="button">-</button>

  <br><hr>

  {{ estado.email }}
  <input type="email" @keyup="alteraEmail">

  <br><hr>

  Saldo: {{ estado.saldo }} <br>
  Transferindo: {{ estado.transferindo }} <br>
  Saldo depois da transferência: {{ mostraSaldoFuturo() }} <br>
  <input :class="{ invalido: !validaValorDeTransferencia() }" @keyup="evento => estado.transferindo = evento.target.value" type="number" placeholder="Quantia para transferir"> <br>
  <button v-if="validaValorDeTransferencia()">transferir</button>
  <span v-else>Valor maior que o saldo</span>
  <br><hr>
  <ul>
    <li v-for="nome in estado.nomes">
      {{ nome }}
    </li>
  </ul>
  <input type="text" @keyup="evento => estado.nomeAInserir = evento.target.value" placeholder="Digite um novo nome">
  <button @click="cadastraValue" type="button">Cadastrar nome</button>

  <h3 v-for="nome in estado.nomes">{{ nome }}</h3>
</template>

<style scoped>
  img {
    max-width: 200px;
  }
  .invalido {
    outline-color: red;
    border-color: red;
  }
</style>
