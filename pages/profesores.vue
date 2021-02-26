<template>
   <div class="container">
      <h1  class="text-primary center">Profesores Hogwarts</h1>
    <Card  v-for="(profesor,i) in profesores"
    :key="i" :personaje="profesor"
    />
  </div>
</template>
<script>
export default {
    created(){
      this.mostrarProfesores()
  },
  data() {
    return{
        profesores: {}
    }
  },
  
  methods: {
    async mostrarProfesores() {
        const result = await this.$axios({
            methods: "get",
            url: `http://hp-api.herokuapp.com/api/characters/staff`
        }).then(res =>{
            this.profesores = res.data
        })
        
    },
  },
};
</script>