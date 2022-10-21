<script setup>
const props = defineProps(['name', 'id']);
const emits = defineEmits(['remove']);

</script>

<template>
    {{name}}
    <button @click="emits ('remove', id)">x</button>
</template>