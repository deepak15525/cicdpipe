<script setup>
const props = defineProps({
    title: String,
    description: String,
    tags: Array
})
</script>

<template>
    <article class="capability-card">
        <div class="capability-icon">◈</div>
        <h3>{{ props.title }}</h3>
        <p>{{ props.description }}</p>
        <div class="tag-list">
            <span v-for="tag in props.tags" :key="tag">{{ tag }}</span>
        </div>
    </article>
</template>
