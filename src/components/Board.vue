<template>
  <div class="board">
    <Column title="To Do" :cards="todoCards" />

    <Column title="In Progress" :cards="progressCards" />
  </div>
</template>

<script setup>
import Column from './Column.vue'

const todoCards = [
  {
    id: 1,
    title: 'Design UI',
    description: 'Create wireframes',
  },
  {
    id: 2,
    title: 'Setup Project',
    description: 'Initialize Vue app',
  },
]

const progressCards = [
  {
    id: 3,
    title: 'API Integration',
    description: 'Connect backend',
  },
]
</script>

<style scoped>
.board {
  display: flex;
  gap: 20px;
  align-items: flex-start;
}
</style>
