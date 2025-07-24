<template>
  <!-- <Home /> -->
  <deuxieme ref="child"></deuxieme>
  <button @click="compteurA++">Incrementer</button>
  <button @click="compteurA--">Décrementer</button>
  <p>{{ compteurA }}</p>

</template>

<script>
import Home from './components/Home.vue';
// import Deuxieme from './components/Deuxieme.vue';

export default {
  data() {
    return {
      compteurA: 0
    }
  },
  watch: {
    compteurA(newVal){
      console.log(`Compteur: ${newVal}`);
      setTimeout(()=>{
        console.log("Reset du compteur A")
        this.compteurA = 0
      }, 3000)
    }
  }
}
</script>

<style lang="scss" scoped>

</style>