<template>
    <h2>HELLO WORD</h2>
    <!-- <user-card v-for="(user, index) in users" :key="index" :user="user" /> -->
    <!-- <user-card :title="cardTitle" :description="cardDescription" /> -->
    
    <p>{{ title || "Titre depuis le parent" }}</p>
    <p>{{ description || "Description depuis le parent" }}</p>

    <user-card @update-title="updateTitle" @update-description="updateDescription" />

</template>

<script >
import UserCard from './UserCard.vue';

export default {
    components: {
        name: 'Sixieme',
        UserCard
    },
    data() {
        return {
            users: [
                { name: "Alice", age: 28 },
                { name: "Boris", age: 35 },
                { name: "Claire", age: 22 },
                { name: "David", age: 40 },
                { name: "Emma", age: 31 }
            ],
            cardTitle: "User Card",
            cardDescription: "This is a user card component that displays user information.",
            title: "",
            description: ""
        }
    },
    methods: {
        updateTitle(newTitle) {
            this.title = newTitle
        },
        updateDescription(newDescription) {
            this.description = newDescription
        }
    },
}

</script>

<style scoped>

</style>