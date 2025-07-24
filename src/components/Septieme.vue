<template>
    <h2>HELLO WORD</h2>
    <!-- <user-card v-for="(user, index) in users" :key="index" :user="user" /> -->
    <!-- <user-card :title="cardTitle" :description="cardDescription" /> -->
    
    <p>{{ title || "Titre depuis le parent" }}</p>
    <p>{{ description || "Description depuis le parent" }}</p>

    <user-card @update-title="updateTitle" @update-description="updateDescription" />

    <CardSlot title="Mon titre">
        <p>Contenu du slot</p>
    </CardSlot>

</template>

<script setup>
import CardSlot from './CardSlot.vue';
import UserCard from './UserCard.vue';


</script>

<style scoped>

</style>