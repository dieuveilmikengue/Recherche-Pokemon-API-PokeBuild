<template>
    <div class="user-card">
        <!-- <h4>{{ user.name }}</h4>
        <p>{{ user.age }} ans</p> -->
        <!-- <h3>{{ title }}</h3>
        <p>{{ description }}</p> -->
        <input v-model="newTitle" placeholder="Entrer un titre" />
        <input v-model="newDescription" placeholder="Entrer une description" />
        <button @click="sendDataToParent">Envoyer</button>
    </div>

    
</template>
<script>
export default {
  name: 'UserCard',
  // props: {
  //   // user: Object,
  //   title: String,
  //   description: String
  // }
  data() {
    return {
      newTitle: "",
      newDescription: ""
    }
  },
  methods: {
    sendDataToParent() {
      this.$emit('update-title', this.newTitle);
      this.$emit('update-description', this.newDescription);
    }
  }
}
</script>

<style scoped>
.user-card {
    border: 1px solid #ccc;
    padding: 10px;
    margin: 15px 0;
    border-radius: 5px;
    background-color: #171616;
}
</style>