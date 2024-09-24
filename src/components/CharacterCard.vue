<script setup lang="ts">
import { Character } from '@/types/character'

const { character } = defineProps<{ character: Character }>()
console.log(character)
</script>
<template>
  <div>
    <h2>{{ character.id }} - {{ character.name }}</h2>
    <p></p>
  </div>
</template>
<style scoped></style>
