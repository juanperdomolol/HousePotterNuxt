<template>
  <div class="container">
    <h1 v-show="selected===null" class="text-primary">¿Quieres Ver los personajes?, selecciona una casa</h1>
    <b-form-select
      v-model="selected"
      :options="options"
      class="sm"
      @change="mostrarPersonajes()"
    ></b-form-select>
    <Card v-for="(personaje, i) in personajes"
    :key="i" :personaje="personaje"
    />
  </div>
</template>
<script>
import Card from "@/components/Card";
export default {
  components: {
    Card,
  },
  data() {
    return {
      selected: null,
      personajes: '',
      options: [
        { value: null, text: "Por favor seleccione una opción" },
        { value: "slytherin", text: "Personajes casa slytherin" },
        { value: "gryffindor", text: "Personajes casa gryffindor" },
        { value: "ravenclaw", text: "Personajes casa ravenclaw" },
        { value: "hufflepuff", text: "Personajes casa hufflepuff" },
      ],
    };
  },
  methods: {
    async mostrarPersonajes() {
      // console.log(this.selected);
      const house = this.selected;

      const result = await this.$axios({
        method: "get",
        url: `http://hp-api.herokuapp.com/api/characters/house/${house}`,
      }).then((res) => {
        this.personajes = res.data;
        // console.log(res.data)
      });
      console.log('Personaje',this.personajes);
    },
  },
};
</script>