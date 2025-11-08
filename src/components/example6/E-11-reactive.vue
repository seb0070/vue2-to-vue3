<template>
  <div>
    <p>Name: {{ person.name }}</p>
    <p>Age: {{ person.age }}</p>
    <button @click="incrementAge">Increment Age</button>
  </div>
</template>

<script>
export default {
  name: 'E11Reactive',
}
</script>

<script setup>
import { reactive } from 'vue'

const person = reactive({
  name: 'John Doe',
  age: 30
})

const incrementAge = () => {
  person.age++
}
</script>
