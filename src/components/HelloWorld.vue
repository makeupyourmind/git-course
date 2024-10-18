<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)

const onCountClick = () => {
  count.value = count.value + 1
}
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <button type="button" @click="onCountClick">count is {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR (hot module replacement)
    </p>
  </div>

  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
