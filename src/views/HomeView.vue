<template>
  <main>
    <div class="counter-show">
      <h2>pinia counter show: </h2>
      <button @click="addNumber">Add Button (pinia action)</button>
      <div>counter (pinia state): {{ counterStore.counter }}</div>
      <div>double counter (pinia getters): {{ counterStore.doubleCount }}</div>
    </div>

    <TheWelcome />
  </main>
</template>

<script setup>
import TheWelcome from '@/components/TheWelcome.vue'
import { useCounterStore } from '../stores/counter'

const counterStore = useCounterStore()
const addNumber = () => {
  counterStore.increment()
}

</script>

<style>
.counter-show {
  padding: 20px;
  border: 1px solid #e5e5e5;
  margin: 30px 0 20px 0;
  border-radius: 8px;
  line-height: 28px;
}

.counter-show h2 {
  margin-bottom:15px;
}
</style>
