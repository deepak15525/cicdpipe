<script setup>
const props = defineProps({
    label: String
})
</script>

<template>
    <div class="skill-pill tilt-card" @pointermove="$emit('tilt', $event)" @pointerleave="$emit('reset', $event)">
        {{ props.label }}
    </div>
</template>
