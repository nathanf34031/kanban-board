<template>
  <div class="column">
    <h2>{{ title }}</h2>

    <Card
      v-for="card in cards"
      :key="card.id"
      :title="card.title"
      :description="card.description"
    />
  </div>
</template>

<script setup>
import Card from './Card.vue'

defineProps({
  title: String,
  cards: {
    type: Array,
    default: () => [],
  },
})
</script>

<style scoped>
.column {
  background: #f4f5f7;
  padding: 1rem;
  width: 300px;
  border-radius: 10px;
}
</style>
