<template>
    <div>
        <h2>HELLO WORD</h2>
        <transition name="fade">
            <p v-if="isVisible">{{ isVisible }}</p>
        </transition>
        <button @click="toggleVisible">Toggle</button>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const isVisible = ref(false)

const toggleVisible = () => {
    isVisible.value = !isVisible.value
}

</script>

<style scoped>

.fade-enter-active, .fade-leave-active{
    transition: opacity 0.5s ease;
}

.fade-enter, .fade-leave-to{
    opacity: 0;
}

</style>