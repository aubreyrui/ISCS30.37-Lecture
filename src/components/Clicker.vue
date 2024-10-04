<template>
    <button @click="increment">Click me</button>
    <p>{{ props.label }} : {{ clicks }}</p>
</template>

<script setup>
  import { ref } from 'vue'

  const props = defineProps({
    label: String
  })

    const clicks = ref(0)

    function increment(evt) {
        console.log(evt)
        clicks.value++
    }
</script>

<style scoped>
</style>