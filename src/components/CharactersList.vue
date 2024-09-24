<script setup lang="ts">
import { ref } from 'vue'
import CharacterCard from '@/components/CharacterCard.vue'
import { Character } from '@/types/character'

const characters = ref<Character[]>([
  { id: '1', name: 'Yoda' },
  { id: '1', name: 'Luke Skywalker' }
])
</script>

<template>
  <p>Choose some characters from the list to be added to your team</p>
  <p v-if="characters.length === 0">No characters available</p>
  <div v-else>
    <CharacterCard v-for="character in characters" :key="character.id" :character="character" />
  </div>
</template>

<style scoped></style>
