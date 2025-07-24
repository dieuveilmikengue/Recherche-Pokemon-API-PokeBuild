<template>
    <h2>HELLO WORD</h2>
    <button @click="increment">Incrementer</button>
    <p>{{ count }}</p>
    <p>
        <strong>{{ doubleCount }}</strong>
    </p>
    <hr>
    <p>{{ state.message }}</p>
    <button @click="updateMessage">Modifier le message</button>
    <hr>
    <p>{{ injectedMessage }}</p>

</template>

<script setup>
import { ref, reactive, computed, watch, onMounted, provide } from 'vue';

const count = ref(0)

const increment = () => {
    count.value++
}

const state = reactive({
    message: "Hello word !"
})

const updateMessage = () => {
    state.message = "Meesage mis à jour !"
}

const doubleCount = computed(() => {
    return count.value * 2
})

watch(count, (newVa, oldVa) => {
    console.log(`Le compteur a changé de ${oldVa} à ${newVa}`)
})

// Quand le composant est monté

onMounted(() => {
    console.log("Composant monté")
})

// provide('message', "Message depuis provider")
// const injectedMessage = inject('message', "Message par défaut si non trouvé")


</script>

<style scoped>

</style>