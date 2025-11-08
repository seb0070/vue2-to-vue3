<template>
  <div>
    <input ref="inputField" type="text" placeholder="Click the button to focus" />
    <button @click="focusInput">Focus Input</button>
  </div>
</template>

<script>
export default {
  name: 'E12RefComponent',
}
</script>

<script setup>
import { ref, onMounted, onBeforeMount, onBeforeUpdate, onUpdated, onBeforeUnmount, onUnmounted } from 'vue'

const inputField = ref(null)

const focusInput = () => {
  inputField.value?.focus()
}

onMounted(() => {
  console.log(inputField)
  if (inputField.value) {
    inputField.value.focus()
  }
})

// 라이프사이클 훅
onBeforeMount(() => console.log('inputField beforeMount'))
onMounted(() => console.log('inputField mounted'))
onBeforeUpdate(() => console.log('inputField beforeUpdate'))
onUpdated(() => console.log('inputField updated'))
onBeforeUnmount(() => console.log('inputField beforeUnmount'))
onUnmounted(() => console.log('inputField unmounted'))
</script>
