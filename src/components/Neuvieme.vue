<template>
    <h2>Liste des Utilisateurs</h2>
    <div v-if="loading">Chargement.....</div>
    <div v-if="error">{{ error }}</div>
    <div v-if="users.length">
        <ul>
            <li v-for="user in users" :key="user.id">{{ user.name }}</li>
        </ul>
    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import axios from 'axios';

const users = ref([])
const loading = ref(false)
const error = ref(null)

const fetchUsers = async () => {
    loading.value = true
    error.value = null
    try {
        const response = await axios.get('https://jsonplaceholder.typicode.com/users')
        users.value = response.data
    }
    catch (err) {
        error.value = "Une erreur c'est produite lors de la recuperation des utilisateurs"
    }
    finally {
        loading.value = false
    }
}

onMounted(fetchUsers)



</script>

<style scoped>

</style>