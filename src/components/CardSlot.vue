<template>
    <div class="card">
        <h2>{{ title }}</h2>
        <div class="content">
            <slot>
                
            </slot>
        </div>
    </div>
</template>

<script setup>
defineProps(
    {
        title: String
    }
)
</script>

<style scoped>

</style>