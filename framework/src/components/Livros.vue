 <template>

 <div id = "livro">
       
   <h3> Número Identificação: {{ni}}</h3>
   <hr>
   <h3> Nome:   {{nome}}</h3>
   <h3> Autor:  {{autor}}</h3> 
  
   </div>
</template>

<script>
export default {
    data(){
        return {
            ni:"",
            nome:"",
            autor: ""

        }
        
    },
  name: 'Livros',
  props: {
    msg: String
  }, 
  
  }

</script>

<style scoped>
#livro {
    background-color: #F2E98E;
    max-width: 600px;
    text-align: justify;
    height: 120px;
    padding: 2%;
    margin-top: 60px;
    margin-left: 25%;
}
</style>
