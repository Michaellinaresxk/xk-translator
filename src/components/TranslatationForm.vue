<template>
  <v-sheet class="mx-auto" width="300">
    <v-form @submit.prevent="handleTranslate">
      <v-text-field
        v-model="translationQuery"

        label="Place your text here"
      ></v-text-field>
      <v-select
      v-model="selectedLanguage"
  label="Select"
  :items="['Polish', 'Spanish', 'English', 'Italian']"
  variant="underlined"
></v-select>
      <v-btn class="mt-2" type="submit" block>Translate</v-btn>
    </v-form>
  </v-sheet>
</template>
<script setup lang="ts">
import { ref } from "vue"

const emit = defineEmits<{
    (e: 'handleTranslate', translationQuery: string, selectedLanguage: string): void
  }>()

const translationQuery = ref('')
const selectedLanguage = ref('')
const handleTranslate = () => {

  emit('handleTranslate', translationQuery.value, selectedLanguage.value )
}
</script>
