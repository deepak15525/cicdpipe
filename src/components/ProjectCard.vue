<script setup>
const props = defineProps({
    project: Object
})
</script>

<template>
    <article class="project-card tilt-card" @pointermove="$emit('tilt', $event)" @pointerleave="$emit('reset', $event)">
        <span class="project-tag">{{ props.project.tag }}</span>
        <h3>{{ props.project.title }}</h3>
        <p>{{ props.project.description }}</p>
        <a class="project-link" :href="props.project.url" target="_blank" rel="noreferrer">Visit website</a>
    </article>
</template>
