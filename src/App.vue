<script setup>
import { ref } from 'vue'

const props = defineProps({
  msg: String,
})

const count = ref(0)
const title = ref(props.msg)

const onCountClick = () => {
  count.value = count.value + 1
}

const onResetClick = () => {
  count.value = 0
}

const onTitleChange = (event) => {
  title.value = event.target.value
}
</script>

<template>
  <h1>{{ title }}</h1>

  <div class="card">
    <button type="button" @click="onCountClick">count is {{ count }}</button>
    <button type="button" @click="onResetClick">Reset</button>
    <div>
      <input v-model="title" placeholder="Change title" />
    </div>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>

  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
.card {
  margin: 20px 0;
}
.card button:nth-child(2) {
  margin-left: 10px;
}
input {
  margin-top: 10px;
  padding: 5px;
}
</style>
