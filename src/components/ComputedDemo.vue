<script setup>
import { ref, computed } from "vue";
let number = ref(5);
let number_quadrat = computed(() => {
    if (number.value % 2){
        return number.value * number.value;
    } else {
        return number.value * number.value * number.value;
}
});

</script>


<template>
    <h3>Computed Demo</h3>
    <p>Zahl: {{number}}</p>
    <p>Zahl Quadriert: {{number_quadrat}}</p>
</template>