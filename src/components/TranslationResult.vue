<template>
  <h2>{{ translatedText }}</h2>
</template>

<script setup lang="ts">
  import { defineProps } from 'vue'

defineProps({
  translatedText: String
})

</script>

<style>
h2 {
margin-top: 25px;
font-weight: bold;
font-size: 2.5em;
}
</style>
