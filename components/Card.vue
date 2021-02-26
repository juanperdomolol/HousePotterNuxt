<template>
  <div class="container">
    <b-col>
      <b-card
        :title="personaje.name"
        :img-src="personaje.image"
        img-heigth="300px"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem"
        class="mb-6 mr-4 mt-5"
        bg-variant="dark"
      >
        <b-card-text  class="text-info">
         {{`Patronus: ${personaje.patronus}\n Nacio el ${personaje.dateOfBirth}`}}
        </b-card-text>
      
      </b-card>
    </b-col>
  </div>
</template>
<script>
export default {
  props: {
    personaje: Object,
    age:0
  },

};
</script>
<style scoped>
.card{
  float: left;
  width: 500px;
  height: 500px;
}

.card-img, .card-img-top{
  width: 320px;
  height: 300px;
}
</style>