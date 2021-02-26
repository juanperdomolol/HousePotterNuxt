<template>
  <div>
    <Navbar />
    <Nuxt />
  </div>
</template>
<script>
import Navbar from "@/components/NavBar"
export default {
  components:{
    Navbar
  }
}
</script>
<style>
body {
  background-image: url(https://wallpapercave.com/wp/wp2900119.jpg);
  background-position: center center;
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
}
</style>
