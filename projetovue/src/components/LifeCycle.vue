<template>
    <h1>Meu nome é {{ nome }}</h1>
</template>

<script>
export default{
   name: 'LifeCycle',
   data(){
     return{
       nome: 'Ainda não sei' 
     }
   },
   created(){
     setTimeout(() => {
        this.nome = 'Pedro Junior'
     }, 1000);
     this.lifeCycle()
   },
   mounted(){
     setTimeout(() => {
        this.nome = 'Andre Luiz'
     }, 2000);
     this.lifeCycle()
   },
   methods:{
     lifeCycle(){
       console.log("Executou");
     }
   } 
}
</script>