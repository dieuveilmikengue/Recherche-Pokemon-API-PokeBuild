<template>
    <h2>Home</h2>
    <h3>{{ message }}</h3>
    <h3>{{ age }}</h3>
    <p>{{ calc(age, 4) }}</p>
    <p>{{ func() }}</p>
    <a v-bind:href="urlGoogle">Lien Google</a><br>
    <img :src="urlImage" alt="" srcset="">
</template>

<script>

    export default {
        data() {
            return {
                message: "Chargement",
                age: 25,
                urlGoogle: "https://www.google.com/",
                urlImage: "https://media.istockphoto.com/id/2203473923/fr/photo/m%C3%A8re-et-fille-se-relaxant-sur-la-plage-de-galets-du-lac-de-garde.webp?b=1&s=612x612&w=0&k=20&c=SVCEm5zWkHpvl9mY37ikIYArLRPrVhkkY_TEDspTMhI="
            }
        },
        methods: {
            calc(a, b){
                return a*b
            },
            func(){
                return this.message + " " + "Dernier"
            }
        }
    }
</script>



<style scoped>

</style>