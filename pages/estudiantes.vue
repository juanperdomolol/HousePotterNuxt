<template>
  <div class="container">
      <h1  class="text-primary center">Estudiantes Hogwarts</h1>
    <Card  v-for="(estudiante,i) in estudiantes"
    :key="i" :personaje="estudiante"
    />
  </div>
</template>
<script>
export default {
    created(){
      this.mostrarEstudiantes()
  },
  data() {
    return{
        estudiantes: {}
    }
  },
  
  methods: {
    async mostrarEstudiantes() {
        const result = await this.$axios({
            methods: "get",
            url: `http://hp-api.herokuapp.com/api/characters/students `
        }).then(res =>{
            this.estudiantes = res.data
        })
        
    },
  },
};
</script>