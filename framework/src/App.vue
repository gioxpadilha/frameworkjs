<template>
  <div id="app">
    <h1>LISTA DE LIVROS</h1>
    <Tabela/> 
  <div id ="form">
  <input type = "number" placeholder="NI" v-model="idField"> <br>
  <input type = "text" placeholder="Nome" v-model="nomeField"> <br>
  <input type = "text" placeholder="Autor" v-model="autorField"> <br>
  </div>
 
  <button  href="#" class="botao" @click="cadastrarlivro"> Cadastrar</button> 
  <Livros/>  
  </div>
  
</template>

<script>
import Livros from './components/Livros.vue'
import Tabela from './components/Tabela.vue'

export default {
  name: 'App',
  data(){
    return{
      idField: "",
      nomeField:"",
      autorField:"", 
      
    }
  },
  livros: [
          {
            Id: 345,
            ni: 5, 
            Nome: "Harry Potter",
            Autor: "JK Rowling"
          }
        ],
  components: {
    Livros,
    Tabela
    
  },
  methods: {
    cadastrarlivro: function (){
      this.livros.push({NI: this.idField, Nome: this.nomeField, Autor: this.autorField, id:Date.now()});
    }
  }
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000408;
  margin-top: 60px;
}
#form {
  margin-top: 0px;
  padding: 0; 
  height: 90px;
  

 
}
.botao {
 box-shadow:inset 0px 1px 0px 0px #9fb4f2;
	background:linear-gradient(to bottom, #7892c2 5%, #476e9e 100%);
	background-color:#7892c2;
	border-radius:6px;
	border:1px solid #4e6096;
	display:inline-block;
	cursor:pointer;
	color:#ffffff;
	font-family:Arial;
	font-size:15px;
	font-weight:bold;
	padding:6px 24px;
	text-decoration:none;
	text-shadow:0px 1px 0px #283966;
}
.botao:hover {
	background:linear-gradient(to bottom, #476e9e 5%, #7892c2 100%);
	background-color:#476e9e;
}
.botao:active {
	position:relative;
	top:1px;
}
</style>
