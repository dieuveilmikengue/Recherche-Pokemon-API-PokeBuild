<template>
    <h3 v-if="statut === 'Reussi'">Reussi</h3>
    <h3 v-else-if="statut === 'Warning'">Avertissemnt</h3>
    <h3 v-else>Erreur</h3>

    <button @click="changeStatut('Reussi')">Succes</button>
    <button @click="changeStatut('Warning')">Warning</button>
    <button @click="changeStatut('Erreur')">Erreur</button>
</template>

<script >
export default {
    data() {
        return {
            statut: "errors"
        }
    },
    methods: {
        changeStatut(newStatut){
            this.statut = newStatut
        }
    }
}

</script>

<style scoped>

</style>