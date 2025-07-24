<template>
    <h2>HELLO WORD</h2>
    <ul>
        <li v-for="(fruit, index) in fruits" :key="index">{{ fruit }}</li>
    </ul>
    <hr>
    <ul>
        <li v-for="(user, index) in users" :key="index">{{ user.name }} - {{ user.age }}</li>
    </ul>
    <hr>
    <ul>
        <li v-for="(team, indexTeam) in teams" :key="indexTeam">
            <strong>{{ team.teamName }}</strong>
            <ul>
                <li v-for="(member, indexMember) in team.members" :key="indexMember">{{ member.name }} - {{ member.age }} ans</li>
            </ul>
        </li>
    </ul>
</template>

<script >
export default {
    data() {
        return {
            fruits: ["Pomme", "Banane", "Orange", "Mangue", "Ananas", "Raisin", "Fraise", "Papaye"],
            users: [
                { name: "Alice", age: 28 },
                { name: "Boris", age: 35 },
                { name: "Claire", age: 22 },
                { name: "David", age: 40 },
                { name: "Emma", age: 31 }
            ],
            teams: [
                {
                    teamName: "Team Alpha",
                    members: [
                    { name: "Alice", age: 28 },
                    { name: "Boris", age: 35 },
                    { name: "Claire", age: 22 }
                    ]
                },
                {
                    teamName: "Team Bravo",
                    members: [
                    { name: "David", age: 40 },
                    { name: "Emma", age: 31 },
                    { name: "Fatima", age: 26 }
                    ]
                },
                {
                    teamName: "Team Charlie",
                    members: [
                    { name: "Grace", age: 30 },
                    { name: "Hassan", age: 33 },
                    { name: "Inès", age: 24 }
                    ]
                }
            ]
        }
    },
}

</script>

<style scoped>

</style>