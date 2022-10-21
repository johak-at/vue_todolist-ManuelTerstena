<script setup>
import {ref, computed} from 'vue';

const name = ref('World');

const nameLength = computed(() => name.value.length);

//mit alert("🦄") Öffnet eine Warnung mit Einhorn 
function unicorn() {
  name.value = name.value + ("🦄");
}
</script>

//Die Funktion :class erstellt mit style neue Klassen und wenn man zum Beispiel Protei rein schreibt wird sie lila mit weißer umrandung. 
<template>
    <h1 :class="name">{{ name }}</h1>
    <p>
      {{ nameLength }}
    </p>
    <input v-model="name" />
    <button @click="unicorn">unicorn</button>
    <button @click="makeRed">Make red</button>
  </template>
  <style>
  .Portei {
    color: purple;
  }
  .Daniel {
    color: blue;
  }
  h1 {
    -webkit-text-stroke-width: 1px;
    -webkit-text-stroke-color: white;
  }
  </style>