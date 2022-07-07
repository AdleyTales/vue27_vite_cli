<template>
  <div>
    <h2>TestView:</h2>
    <div>num fen: {{ numFen }}</div>
    <div>num yuan: ¥{{ numYuan }}</div>
    <div>
      <button @click="handleAddNumFen">Click Button</button>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, computed } from 'vue'

let numFen = ref(1000);

onMounted(() => {
  console.log('------  This is TestView  👌 ------');
})

// handle click button to add num 100 per time
const handleAddNumFen = () => {
  numFen.value += 100;
}

let numYuan =  computed(() => {
  return (numFen.value/100).toFixed(2)
})

</script>

