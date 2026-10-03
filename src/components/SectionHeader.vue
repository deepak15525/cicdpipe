<script setup>
const props = defineProps({
    tag: String,
    title: String
})
</script>

<template>
    <div class="section-heading">
        <p class="section-tag">{{ props.tag }}</p>
        <h2>{{ props.title }}</h2>
    </div>
</template>
