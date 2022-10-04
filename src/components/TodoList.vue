<script setup>
import { ref } from "vue";
const list = ref([]);
const newItem = ref("");
function addIem() {
  list.value.push(newItem.value);
  newItem.value = "";
}
function Clear() {
  list.value = [];
}
</script>

<template>
    <h1>TodoList</h1>
    <input type="text" v-model="newItem" />
    <button @click="addIem">Add</button>
    <button @click="list = []">Clear</button>
    <ul>
        <li v-for="item in list" :key="item">{{item}}</li>
    </ul>
</template>_

