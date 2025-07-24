<template>
  <!-- <Home /> -->
  <deuxieme ref="child"></deuxieme>
  <button @click="compteurA++">Incrementer</button>
  <button @click="compteurA--">Décrementer</button>
  <p>{{ compteurA }}</p>
  <br/>
  <deuxieme ref="child"></deuxieme>
  <button @click="compteurB++">Incrementer</button>
  <button @click="compteurB--">Décrementer</button>
  <p>{{ compteurB }}</p>
  <br/>
  <p>{{ statutMethod() }}</p>
  <p>{{ statutComputed }}</p>
</template>

<script>
import Home from './components/Home.vue';
import Deuxieme from './components/Deuxieme.vue';

export default {
  data() {
    return {
      compteurA: 0,
      compteurB: 0
    }
  },
  methods: {
    statutMethod(){
      return this.compteurA > 10 ? "Superieur" : "Inferieure";
    }
  },
  computed: {
    statutComputed(){
      return this.compteurA > 10 ? "Superieur" : "Inferieure";
    }
  },
}
</script>

<style lang="scss" scoped>

</style>