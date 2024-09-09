<script setup lang="ts">
import { ref } from "vue"
import TranslationForm from "../components/TranslatationForm.vue"
import TranslationResult from "../components/TranslationResult.vue"


const translatedText = ref('')
const translateQuery = (translationQuery: string, selectedLanguage: string) => {
  console.log(selectedLanguage, translationQuery )
}

</script>

<template>
  <main>
     <TranslationForm @handleTranslate="translateQuery" />
     <TranslationResult :translatedText="translatedText" />
  </main>
</template>
