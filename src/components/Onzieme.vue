<template>
    <div>
        <h2>TRANSITION GROUPE</h2>
    </div>
    <div>
        <button @click="addItem">Ajouter un element</button>
        <button @click="removeItem" :disabled="items.length === 0">Supprimer un element</button>
    </div>
    <div>
        <ul>
            <li v-for="item in items" :key="item">{{ item }}</li>
        </ul>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const items = ref([])

let nextId = ref(1)

const addItem = () => {
    items.value.push(`Element ${nextId.value++}`)
}

const removeItem = () => {
    items.value.pop()
}

</script>

<style scoped>

</style>